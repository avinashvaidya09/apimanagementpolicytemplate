# API Management policy template for OAuth using Process Integration Runtime

Each policy is listed and described below

1. lookupOAuthToken - Using LookupCache policy, checks if access token is available in cache.
2. extractRequestHeader - Using ExtractVariables policy, extracts the client id and client secret from the request headers.
3. getBTPOAuthMetadata - Using KeyValueMapOperations policy, finds the BTP oauth token url saved in the key value map
4. setAuthorization - Using BasicAuthentication policy, creates Authorization object.
5. callBTPOAuthService - Using ServiceCallout policy, calls external BTP OAuth token url.
6. raiseException - Using raiseException policy, raises exception if BTP OAuth token url returns exception.
7. extractVariablesFromOAuthResponse - Using ExtractVariables policy, extracts token response.
8. populateOAuthToken - Using PopulateCache policy, populates access token in cache which will be used by point 1.
