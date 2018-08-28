---
swagger: "2.0"
x-collection-name: Dezrez
x-complete: 0
info:
  title: Dezrez Attaches an existing document to a milestone
  version: 1.0.0
  description: Attaches an existing document to a milestone.
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
    put:
      summary: Update an auction role milestone
      description: Update an auction role milestone.
      operationId: AuctionRole_SaveAuctionMilestoneByroleIdBydataContract
      x-api-path-slug: apiroleauctionmilestoneroleid-put
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
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
      - Milestone
    post:
      summary: Add a new auction role milestone
      description: Add a new auction role milestone.
      operationId: AuctionRole_AddAuctionMilestoneByroleIdBydataContract
      x-api-path-slug: apiroleauctionmilestoneroleid-post
      parameters:
      - in: body
        name: dataContract
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
      responses:
        200:
          description: OK
      tags:
      - New
      - Auction
      - Role
      - Milestone
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
  /api/progression/lettings/{id}/resetmilestones:
    post:
      summary: Reset tenant role milestones back to agency defaults
      description: Reset tenant role milestones back to agency defaults.
      operationId: LettingsProgression_ResetRoleMilestonesToDefaultByid
      x-api-path-slug: apiprogressionlettingsidresetmilestones-post
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
      - Reset
      - Tenant
      - Role
      - Milestones
      - Back
      - To
      - Agency
      - Defaults
  /api/progression/lettings/resetdefaultmilestones:
    post:
      summary: Reset agency default milestones back to global defaults
      description: Reset agency default milestones back to global defaults.
      operationId: LettingsProgression_ResetMilestonesToDefault
      x-api-path-slug: apiprogressionlettingsresetdefaultmilestones-post
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Reset
      - Agency
      - Default
      - Milestones
      - Back
      - To
      - Global
      - Defaults
  /api/agency/milestoneconfigurations:
    get:
      summary: Get the milestone configurations for an agency
      description: Get the milestone configurations for an agency.
      operationId: Agency_MilestoneConfigurations
      x-api-path-slug: apiagencymilestoneconfigurations-get
      parameters:
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Milestone
      - Configurationsan
      - Agency
  /api/role/auction/milestone/{roleId}/{milestoneId}:
    delete:
      summary: Delete a custom auction milestone
      description: Delete a custom auction milestone.
      operationId: AuctionRole_DeleteAuctionMilestoneByroleIdBymilestoneId
      x-api-path-slug: apiroleauctionmilestoneroleidmilestoneid-delete
      parameters:
      - in: path
        name: milestoneId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Auction
      - Milestone
  /api/milestone/{id}/uploadandattachdocument:
    post:
      summary: Allows you to upload a document and attach it directly to a milestone.
      description: Allows you to upload a document and attach it directly to a milestone..
      operationId: Milestone_UploadAndAttachDocumentByidBydocumentDetailsContract
      x-api-path-slug: apimilestoneiduploadandattachdocument-post
      parameters:
      - in: body
        name: documentDetailsContract
        description: Document save command
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
        description: The milestone Id
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Allows
      - You
      - To
      - Upload
      - Document
      - Attach
      - It
      - Directly
      - To
      - Milestone
  /api/milestone/{id}/attachdocument:
    put:
      summary: Attaches an existing document to a milestone
      description: Attaches an existing document to a milestone.
      operationId: Milestone_AttachDocumentByidBydocumentId
      x-api-path-slug: apimilestoneidattachdocument-put
      parameters:
      - in: query
        name: documentId
        description: The id of the document to attach
      - in: path
        name: id
        description: The id of the milestone to attach the document to
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Attaches
      - Existing
      - Document
      - To
      - Milestone
  /api/milestone/{id}/detachdocument:
    put:
      summary: Detaches a document from a milestone
      description: Detaches a document from a milestone.
      operationId: Milestone_DetachDocumentByidBydocumentId
      x-api-path-slug: apimilestoneiddetachdocument-put
      parameters:
      - in: query
        name: documentId
        description: The id of the document to detach
      - in: path
        name: id
        description: The id of the milestone to detach the document from
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Detaches
      - Document
      - From
      - Milestone
  /api/progression/milestonessummary:
    get:
      summary: Get a progression milestone summary for the given progression role
      description: Get a progression milestone summary for the given progression role.
      operationId: Progression_MilestonesSummaryByprogressionRoleIdBymilestoneLeaseTypeBymilestoneCategoryType
      x-api-path-slug: apiprogressionmilestonessummary-get
      parameters:
      - in: query
        name: milestoneCategoryType
      - in: query
        name: milestoneLeaseType
      - in: query
        name: progressionRoleId
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Progression
      - Milestone
      - Summarythe
      - Given
      - Progression
      - Role
  /api/progression/{id}/deletemilestone/{milestoneId}:
    delete:
      summary: Delete milestone on Progression role
      description: Delete milestone on progression role.
      operationId: Progression_DeleteProgressionMilestoneByidBymilestoneId
      x-api-path-slug: apiprogressioniddeletemilestonemilestoneid-delete
      parameters:
      - in: path
        name: id
        description: Progression Role Id
      - in: path
        name: milestoneId
        description: Milestone Id to be deleted
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Milestone
      - "On"
      - Progression
      - Role
  /api/progression/milestone/addnote:
    post:
      summary: Add a note to an individual progression milestone
      description: Add a note to an individual progression milestone.
      operationId: Progression_AddMilestoneNoteBynoteDataContract
      x-api-path-slug: apiprogressionmilestoneaddnote-post
      parameters:
      - in: body
        name: noteDataContract
        description: Notes to be added
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Individual
      - Progression
      - Milestone
  /api/progression/milestone/{roleId}/add:
    post:
      summary: Add a milestone to a role.
      description: Add a milestone to a role..
      operationId: Progression_AddProgressionMilestoneByaddProgressionMilestoneDataContractByroleId
      x-api-path-slug: apiprogressionmilestoneroleidadd-post
      parameters:
      - in: body
        name: addProgressionMilestoneDataContract
        description: The milestone to add
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: path
        name: roleId
        description: Id of the role to add the milestone to
      responses:
        200:
          description: OK
      tags:
      - Milestone
      - To
      - Role
  /api/progression/milestones/reset:
    put:
      summary: Add a note to an individual progression milestone
      description: Add a note to an individual progression milestone.
      operationId: Progression_ResetRoleMilestonesBypurchasingRoleIdByroleId
      x-api-path-slug: apiprogressionmilestonesreset-put
      parameters:
      - in: query
        name: purchasingRoleId
        description: The purchasing role ID
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      - in: query
        name: roleId
        description: Sales role ID
      responses:
        200:
          description: OK
      tags:
      - Note
      - To
      - Individual
      - Progression
      - Milestone
  /api/progression/milestones/order:
    put:
      summary: Set milestone orders
      description: Set milestone orders.
      operationId: Progression_SetMilestoneOrderBypurchasingRoleIdBymilestoneOrders
      x-api-path-slug: apiprogressionmilestonesorder-put
      parameters:
      - in: body
        name: milestoneOrders
        description: Collection of milestone orders
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: purchasingRoleId
        description: The purchasing role ID
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Set
      - Milestone
      - Orders
  /api/progression/milestones/add:
    put:
      summary: Save a new milestone
      description: Save a new milestone.
      operationId: Progression_AddMilestoneDataContractBypurchasingRoleIdBymilestoneDatacontract
      x-api-path-slug: apiprogressionmilestonesadd-put
      parameters:
      - in: body
        name: milestoneDatacontract
        description: Collection of milestone orders
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: purchasingRoleId
        description: The purchasing role ID
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Save
      - New
      - Milestone
  /api/progression/milestones/remove:
    put:
      summary: Remove a new milestone
      description: Remove a new milestone.
      operationId: Progression_RemoveMilestoneBypurchasingRoleIdBymilestoneId
      x-api-path-slug: apiprogressionmilestonesremove-put
      parameters:
      - in: query
        name: milestoneId
        description: Id of milestone to remove
      - in: query
        name: purchasingRoleId
        description: The purchasing role ID
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Remove
      - New
      - Milestone
  /api/role/auction/milestone/{roleId}/create:
    put:
      summary: Create default milestones for role if they dont exist
      description: Create default milestones for role if they dont exist.
      operationId: AuctionRole_PopulateAuctionMilestonesByroleId
      x-api-path-slug: apiroleauctionmilestoneroleidcreate-put
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
      - Default
      - Milestonesrole
      - If
      - They
      - Dont
      - Exist
  /api/progression/getallmilestones:
    get:
      summary: Get all progression milestones for the given progression role
      description: Get all progression milestones for the given progression role.
      operationId: Progression_GetAllProgressionMilestonesByprogressionRoleIdBypageSizeBypageNumberBymilestoneLeaseType
      x-api-path-slug: apiprogressiongetallmilestones-get
      parameters:
      - in: query
        name: milestoneCategoryType
      - in: query
        name: milestoneLeaseType
      - in: query
        name: milestoneStatus
      - in: query
        name: pageNumber
      - in: query
        name: pageSize
      - in: query
        name: progressionRoleId
      - in: query
        name: progressionRoleType
      - in: header
        name: Rezi-Api-Version
        description: Specifies which version of the API to call
      responses:
        200:
          description: OK
      tags:
      - Progression
      - Milestonesthe
      - Given
      - Progression
      - Role
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