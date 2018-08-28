---
swagger: "2.0"
x-collection-name: AWS WorkSpaces
x-complete: 0
info:
  title: AWS WorkSpaces Service API Stop Workspaces
  version: 1.0.0
  description: Stops the specified WorkSpaces.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=CreateWorkspaces:
    get:
      summary: Create Workspaces
      description: Creates one or more WorkSpaces.
      operationId: createWorkspaces
      x-api-path-slug: actioncreateworkspaces-get
      parameters:
      - in: query
        name: Workspaces
        description: An array of structures that specify the WorkSpaces to create
        type: string
      responses:
        200:
          description: OK
      tags:
      - ""
  /?Action=DescribeWorkspaceDirectories:
    get:
      summary: Describe Workspace Directories
      description: Retrieves information about the AWS Directory Service directories
        in the region that are registered with Amazon WorkSpaces and are available
        to your account.
      operationId: describeWorkspaceDirectories
      x-api-path-slug: actiondescribeworkspacedirectories-get
      parameters:
      - in: query
        name: DirectoryIds
        description: An array of strings that contains the directory identifiers to
          retrieve information for
        type: string
      - in: query
        name: NextToken
        description: The NextToken value from a previous call to this operation
        type: string
      responses:
        200:
          description: OK
      tags:
      - Workspace Directories
  /?Action=DescribeWorkspaces:
    get:
      summary: Describe Workspaces
      description: Obtains information about the specified WorkSpaces.
      operationId: describeWorkspaces
      x-api-path-slug: actiondescribeworkspaces-get
      parameters:
      - in: query
        name: BundleId
        description: The identifier of a bundle to obtain the WorkSpaces for
        type: string
      - in: query
        name: DirectoryId
        description: Specifies the directory identifier to which to limit the WorkSpaces
        type: string
      - in: query
        name: Limit
        description: The maximum number of items to return
        type: string
      - in: query
        name: NextToken
        description: The NextToken value from a previous call to this operation
        type: string
      - in: query
        name: UserName
        description: Used with the DirectoryId parameter to specify the directory
          user for whom to         obtain the WorkSpace
        type: string
      - in: query
        name: WorkspaceIds
        description: An array of strings that contain the identifiers of the WorkSpaces
          for which to retrieve information
        type: string
      responses:
        200:
          description: OK
      tags:
      - Workspaces
  /?Action=RebootWorkspaces:
    get:
      summary: Reboot Workspaces
      description: Reboots the specified WorkSpaces.
      operationId: rebootWorkspaces
      x-api-path-slug: actionrebootworkspaces-get
      parameters:
      - in: query
        name: RebootWorkspaceRequests
        description: An array of structures that specify the WorkSpaces to reboot
        type: string
      responses:
        200:
          description: OK
      tags:
      - Workspaces
  /?Action=RebuildWorkspaces:
    get:
      summary: Rebuild Workspaces
      description: Rebuilds the specified WorkSpaces.
      operationId: rebuildWorkspaces
      x-api-path-slug: actionrebuildworkspaces-get
      parameters:
      - in: query
        name: RebuildWorkspaceRequests
        description: An array of structures that specify the WorkSpaces to rebuild
        type: string
      responses:
        200:
          description: OK
      tags:
      - Workspaces
  /?Action=StartWorkspaces:
    get:
      summary: Start Workspaces
      description: Starts the specified WorkSpaces.
      operationId: startWorkspaces
      x-api-path-slug: actionstartworkspaces-get
      parameters:
      - in: query
        name: StartWorkspaceRequests
        description: The requests
        type: string
      responses:
        200:
          description: OK
      tags:
      - Workspaces
  /?Action=StopWorkspaces:
    get:
      summary: Stop Workspaces
      description: Stops the specified WorkSpaces.
      operationId: stopWorkspaces
      x-api-path-slug: actionstopworkspaces-get
      parameters:
      - in: query
        name: StopWorkspaceRequests
        description: The requests
        type: string
      responses:
        200:
          description: OK
      tags:
      - Workspaces
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---