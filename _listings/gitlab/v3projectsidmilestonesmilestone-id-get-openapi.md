---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Get Projects Milestones Milestone
  version: 1.0.0
  description: Get projects milestones milestone.
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/projects/{id}/milestones:
    get:
      summary: Get Projects Milestones
      description: Get a list of project milestones
      operationId: getV3ProjectsIdMilestones
      x-api-path-slug: v3projectsidmilestones-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: formData
        name: iid
        description: The IID of the milestone
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      - in: query
        name: state
        description: Return active, closed, or all milestones
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Milestones
    post:
      summary: Post Projects Milestones
      description: Create a new project milestone
      operationId: postV3ProjectsIdMilestones
      x-api-path-slug: v3projectsidmilestones-post
      parameters:
      - in: formData
        name: description
        description: The description of the milestone
      - in: formData
        name: due_date
        description: The due date of the milestone
      - in: path
        name: id
        description: The ID of a project
      - in: formData
        name: start_date
        description: The start date of the milestone
      - in: formData
        name: title
        description: The title of the milestone
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Milestones
  /v3/projects/{id}/milestones/{milestone_id}:
    get:
      summary: Get Projects Milestones Milestone
      description: Get projects milestones milestone.
      operationId: getV3ProjectsIdMilestonesMilestoneId
      x-api-path-slug: v3projectsidmilestonesmilestone-id-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: milestone_id
        description: The ID of a project milestone
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Milestones
      - Milestone
    put:
      summary: Put Projects Milestones Milestone
      description: Update an existing project milestone
      operationId: putV3ProjectsIdMilestonesMilestoneId
      x-api-path-slug: v3projectsidmilestonesmilestone-id-put
      parameters:
      - in: formData
        name: description
        description: The description of the milestone
      - in: formData
        name: due_date
        description: The due date of the milestone
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: milestone_id
        description: The ID of a project milestone
      - in: formData
        name: start_date
        description: The start date of the milestone
      - in: formData
        name: state_event
        description: The state event of the milestone
      - in: formData
        name: title
        description: The title of the milestone
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Milestones
      - Milestone
  /v3/projects/{id}/milestones/{milestone_id}/issues:
    get:
      summary: Get Projects Milestones Milestone Issues
      description: Get all issues for a single project milestone
      operationId: getV3ProjectsIdMilestonesMilestoneIdIssues
      x-api-path-slug: v3projectsidmilestonesmilestone-idissues-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: milestone_id
        description: The ID of a project milestone
      - in: query
        name: page
        description: Current page number
      - in: query
        name: per_page
        description: Number of items per page
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Milestones
      - Milestone
      - Issues
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