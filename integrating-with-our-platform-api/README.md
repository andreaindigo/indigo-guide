---
icon: plug
---

# Integrating with Our Platform API

Indigo.ai’s platform offers robust **GraphQL-based APIs** that enable seamless interaction with your AI Agents. Whether you're looking to automate workflows, extract data for analysis, or enhance integrations across your tech stack, our API provides all the tools you need to extend your virtual assistant's capabilities.

## 🔧 What You Can Do with the API

Our APIs support a wide range of use cases, including:

* **Data Extraction**: Retrieve detailed records of conversations, agent responses, and user feedback to integrate with internal systems.
* **Bulk Updates**: Automate large-scale updates to your AI Agents data sources, like knowledge base articles and user profiles.
* **Custom Analytics**: Build personalized dashboards using real-time chat, agent, and user data.

## 📘 API Documentation & Endpoint

#### 🔗 **Documentation**

You can find the latest technical details and schema definitions here: [Indigo.ai API docs](https://studio.apollographql.com/public/indigoai/variant/latest/home).

The APIs are primarily based on **GraphQL**. You can access them via a dedicated GraphQL client or any standard HTTP client by following [the appropriate format](https://graphql.org/learn/serving-over-http/).

#### 🌐 **API Endpoint**

All API requests should be directed to: `https://platform.indigo.ai/graphql`

Use the **POST** HTTP method for all calls.

## 🔐 Authentication

Authentication is handled via **personal access tokens**. All requests must include an `Authorization` header in the following format:

```http
Authorization: Bearer pat-*your_pat_value*
```

{% hint style="warning" %}
If you're interested in getting access to our API, please [contact us](../need-help/our-customer-success-team.md)!&#x20;

Note that API access is a premium feature and incurs an additional cost.
{% endhint %}

## Pagination Model

The API implements the [**Relay-style cursor-based pagination**](https://studio.apollographql.com/public/indigoai/variant/latest/home) model. Each query response includes `endCursor` and `hasNextPage` fields within the `pageInfo` object, enabling efficient traversal of large datasets through sequential requests.

## Example Use Cases

Here are practical examples of how you can leverage our APIs.

### 📤 Get All Chats from a Workspace

Use the [`conversations` query](https://studio.apollographql.com/public/indigoai/variant/latest/schema/reference?query=conversations#conversations) to retrieve all chat sessions:

```graphql
query Conversations(
    $projectId: Int_ID!
    $order: SortType
    $cursor: String
  ) {
    conversations(
      projectId: $projectId
      env: PRODUCTION
      order: $order
      first: 50
      after: $cursor
    ) {
      edges {
        node {
          conversationId
        }
      }
      pageInfo {
        endCursor
        hasNextPage
      }
      totalCount
    }
  }
```

#### Output structure

Once the query is executed with the required parameters, the API returns a response structured as follows:

```json
{
    "data": {
        "conversations": {
            "edges": [
                {
                    "node": {
                        "conversationId": "1734638990"
                    }
                },
                {
                    "node": {
                        "conversationId": "1732637760"
                    }
                },
                {
                    "node": {
                        "conversationId": "1736755112"
                    }
                },
								(...)
            ],
            "pageInfo": {
                "endCursor": "dmVyc2VtY3Vyc20yOjE3MzQyNzA0LFBST0RVE1RJT04=",
                "hasNextPage": true
            },
            "totalCount": 1017
        }
    }
}
```

### 💬 Get All Messages from a Chat

Once you have a `conversationId`, use the [`messages` query](https://studio.apollographql.com/public/indigoai/variant/latest/schema/reference/objects/RootQueryType?query=messages#messages) to extract every message:

```graphql
query Messages(
    $conversationId: Int_ID!
    $before: String
    $last: Int
  ) {
    messages(
      conversationId: $conversationId
      env: PRODUCTION
      showFeedback: true
      last: $last
      before: $before
    ) {
      edges {
        node {
          id
			    content
			    sender {
			      id
			    }
			    insertedAt
			    conversationId
			    feedback
			    read
        }
      }
      pageInfo {
        endCursor
        hasNextPage
      }
      totalCount
    }
  }
```

#### Output structure

```json
{
    "data": {
        "messages": {
            "edges": [
                {
                    "node": {
                        "content": {
                            "hidden": false,
                            "sender": "642981ee976e2w9fba60hf17",
                            "text": "OK GRAZIE",
                            "timestamp": 1680181239415,
                            "type": "text"
                        },
                        "conversationId": "17536399072",
                        "feedback": null,
                        "id": "37029883512",
                        "insertedAt": "2023-03-30T13:01:16",
                        "read": null,
                        "sender": {
                            "id": "17356397290"
                        }
                    }
                },
                {
                    "node": {
                        "content": {
                            "messages": [
                                {
                                    "input": {
                                        "type": "text"
                                    },
                                    "messages": [
                                        {
                                            "data": {
                                                "text": "Per ulteriori le consigliamo di contattare il nostro ufficio"
                                            },
                                            "type": "text"
                                        }
                                    ]
                                }
                            ]
                        },
                        "conversationId": "12363590",
                        "feedback": null,
                        "id": "378200345",
                        "insertedAt": "2023-03-30T13:00:43",
                        "read": "2023-03-30T13:00:07",
                        "sender": null
                    }
                }
                (...)
            ],
            "pageInfo": {
                "endCursor": "dmVyc2VfY3Vyc00yOjM3MDI4jHM1",
                "hasNextPage": false
            },
            "totalCount": 12
        }
    }
}
```

Messages are returned in **reverse chronological order** (newest first). To navigate through paginated results, use the `before` argument in the same way you would use `after`.

Within each message object:

* The `sender` field indicates the origin of the message. If the value is `null`, the message was sent by the virtual assistant; otherwise, it contains an object representing the user (`bot_user.id`).
* The actual message content is located in the `content` field.

### 👥 Get All Users in a Workspace

Use the [`userRoles` query](https://studio.apollographql.com/public/indigoai/variant/latest/schema/reference/objects/RootQueryType?query=userRoles#userRoles) to retrieve users and their roles:

```graphql
query {
    userRoles(
      projectId: 39
      first: 100
    ) {
      edges {
        node {
	        role {
	          label
	        }
	        user {
            id
            email
          }
        }
      }
      pageInfo {
        endCursor
        hasNextPage
      }
      totalCount
    }
  }

```

#### Output structure

```json
{
    "data": {
        "users": {
            "edges": [
                {
                    "node": {
                        "role": {
                            "label": "admin"
                        },
                        "user": {
                            "id": "1734638990",
                            "email": "test@test.it"
                        }
                    }
                },
								(...)
            ],
            "pageInfo": {
                "endCursor": "dmVyc2VtY3Vyc20yOjE3MzQyNzA0LFBST0RVE1RJT04=",
                "hasNextPage": true
            },
            "totalCount": 20
        }
    }
}
```
