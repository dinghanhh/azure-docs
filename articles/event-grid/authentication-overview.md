---
title: Authenticate clients publishing events to Event Grid custom topics, domains, and partner namespaces.
description: This article describes different ways of authenticating clients publishing events to Event Grid custom topics, domains, and partner namespaces. 
ms.topic: conceptual
ms.date: 08/10/2021
---

# Client authentication when publishing events to Event Grid
Authentication for clients publishing events to Event Grid is supported using the following methods:

- Azure Active Directory (Azure AD)
- Access key or shared access signature (SAS)

## Authenticate using Azure Active Directory (preview)
Azure AD integration for Event Grid resources provides Azure role-based access control (RBAC) for fine-grained control over a client’s access to resources. You can use Azure RBAC to grant permissions to a security principal, which may be a user, a group, or an application service principal. The security principal is authenticated by Azure AD to return an OAuth 2.0 token. The token can be used to authorize a request to access Event Grid resources (topics, domains, or partner namespaces). For detailed information, see [Authenticate and authorize with the Microsoft Identity platform](authenticate-with-active-directory.md).


> [!IMPORTANT]
> Authenticating and authorizing users or applications using Azure AD identities provides superior security and ease of use over key-based and shared access signatures (SAS) authentication. With Azure AD, there is no need to store secrets used for authentication in your code and risk potential security vulnerabilities. We strongly recommend that you use Azure AD with your Azure Event Grid event publishing applications.

> [!NOTE]
> Azure AD authentication support by Azure Event Grid has been released as preview. 
> Azure Event Grid on Kubernetes does not support Azure AD authentication yet. 

## Authenticate using access keys and shared access signatures
You can authenticate clients that publish events to Azure Event Grid topics, domains, partner namespaces using **access key** or **Shared Access Signature (SAS)** token. For more information, see [Using access keys or using Shared Access Signatures (SAS)](authenticate-with-access-keys-shared-access-signatures.md). 
   

## Next steps
This article deals with authentication when **publishing** events to Event Grid (event ingress). To learn about authenticating when **delivering** events (event egress), see [Authenticate event delivery to event handlers](security-authentication.md). 

