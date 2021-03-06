# Ballerina GitHub Connector - Tests

###### GitHub brings together the world's largest community of developers to discover, share, and build better software. From open source projects to private team repositories, GitHub is an all-in-one platform for collaborative development.

The Ballerina GitHub connector allow users to access the GitHub API through ballerina. This connector uses the GitHub GraphQL API v4.0

|Ballerina Version | Connector Version | GitHub API Version |
|------------------|-------------------| ------------------ |
|0.970.0-alpha5-SNAPSHOT | 0.9.4 | v4 |

## Running github4.tests

All the github4.tests inside this package will make HTTP calls to the GitHub GraphQL API v4. If the HTTP call fails, then so will the test case.

In order to run the github4.tests, the user will need to have a GitHub Personal Access Token. The token can be obtained by visiting

**https://github.com/{profile} -> Settings -> Developer Settings -> Personal access tokens**

and provide the obtained token to the GitHubConnectorConfiguration as follows

```ballerina
endpoint github4:Client githubConnectorEP {
    accessToken:"<ACCESS_TOKEN>",
    clientEndpointConfiguration: {}
};
```

Run tests :
```
ballerina test github4
```