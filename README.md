# ![LOGO](logo.png) Medium.com **flow**ground Connector

## Description

A generated **flow**ground connector for the Medium.com API (version 1.0.0).

Generated from: https://api.apis.guru/v2/specs/medium.com/1.0.0/swagger.json<br/>
Generated at: 2019-05-07T17:42:58+03:00

## API Description

Medium’s unofficial API documentation using OpenAPI specification.

# Official API
Official API document can also be viewed for most up to date API spec at [https://github.com/Medium/medium-api-docs](https://github.com/Medium/medium-api-docs).

Developer Blog - [Welcome to the Medium API](https://medium.com/blog/welcome-to-the-medium-api-3418f956552)


## Authorization

Supported authorization schemes:
- API Key- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### User details

> Returns details of the user who has granted permission to the application.

*Tags:* `Users`

### Contributors of Publication

> This endpoint returns a list of contributors for a given publication. In other words, a list of Medium users who are allowed to publish under a publication, as well as a description of their exact role in the publication (for now, either an editor or a writer).

*Tags:* `Publications` `Users`

#### Input Parameters
* `publicationId` - _required_ - A unique identifier for the publication.

### Create Publication Post

> creating a post and associating it with a publication on Medium. The request also shows this association, considering posts a collection of resources under a publication<br/>
> <br/>
> There are additional rules around publishing that each request to this API must respect:<br/>
>   - If the authenticated user is an 'editor' for the publication, they can create posts with any publish status. Posts published as 'public' or 'unlisted' will appear in collection immediately, while posts created as 'draft' will remain in pending state under publication.<br/>
>   - If the authenticated user is a 'writer' for the chosen publication, they can only create a post as a 'draft'. That post will remain in pending state under publication until an editor for the publication approves it.<br/>
>   - If the authenticated user is neither a 'writer' nor an 'editor', they are not allowed to create any posts in a publication.

*Tags:* `Posts` `Publications`

#### Input Parameters
* `publicationId` - _required_ - Here publicationId is the id of the publication the post is being created under. The publicationId can be acquired from the API for listing user's publications.

### Create User Post

> Creates a post on the authenticated user's profile.

*Tags:* `Users` `Posts`

#### Input Parameters
* `authorId` - _required_ - authorId is the user id of the authenticated user.

### User's publications

> Returns a full list of publications that the user is related to in some way. This includes all publications the user is subscribed to, writes to, or edits.

*Tags:* `Publications`

#### Input Parameters
* `userId` - _required_ - A unique identifier for the user.

## License

**flow**ground :- Telekom iPaaS / medium-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
