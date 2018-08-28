---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Set tenant role milestones as the defaults for agency
  version: 1.0.0
  description: Set tenant role milestones as the defaults for agency.
host: api.dezrez.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/role/auction/milestone/{roleId}:
    get:
      summary: Get auction role milestones
      description: Get auction role milestones.
      operationId: AuctionRole_GetRoleMilestonesByroleId
      x-api-path-slug: apiroleauctionmilestoneroleid-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
      responses:
        200:
          description: OK
      tags:
      - Auction
      - Role
      - Milestones
  /api/progression/lettings/{id}/setdefaultmilestones:
    post:
      summary: Set tenant role milestones as the defaults for agency
      description: Set tenant role milestones as the defaults for agency.
      operationId: LettingsProgression_SetRoleMilestonesAsDefaultByid
      x-api-path-slug: apiprogressionlettingsidsetdefaultmilestones-post
      parameters:
      - in: path
        name: id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Tenant
      - Role
      - Milestones
      - As
      - Defaultsagency
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