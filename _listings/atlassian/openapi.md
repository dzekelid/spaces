swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /space:
    get:
      summary: Get spaces
      description: |-
        Returns all spaces. The returned spaces are ordered alphabetically in
        ascending order by space key.

        **[Permissions](https://confluence.atlassian.com/x/_AozKw) required**:
        Permission to access the Confluence site ('Can use' global permission).
        Note, the returned list will only contain spaces that the current user
        has permission to view.
      operationId: com.atlassian.confluence.plugins.restapi.resources.SpaceResource.getSpaces_get
      x-api-path-slug: space-get
      parameters:
      - in: query
        name: expand
        description: 'A multi-value parameter indicating which properties of the spaces
          toexpand, where:  - `settings` returns the settings for the space, similar
          to [Get space settings](#api-space-spaceKey-settings-get)'
      - in: query
        name: favourite
        description: Filter the results to the favourite spaces of the user specified
          by`favouriteUserKey`
      - in: query
        name: favouriteUserKey
        description: The userKey of the user, whose favourite spaces are used to filterthe
          results when using the `favourite` parameter
      - in: query
        name: label
        description: Filter the results to spaces based on their label
      - in: query
        name: limit
        description: The maximum number of spaces to return per page
      - in: query
        name: spaceKey
        description: The key of the space to be returned
      - in: query
        name: start
        description: The starting index of the returned spaces
      - in: query
        name: status
        description: Filter the results to spaces based on their status
      - in: query
        name: type
        description: Filter the results to spaces based on their type
      responses:
        200:
          description: OK
      tags:
      - Spaces