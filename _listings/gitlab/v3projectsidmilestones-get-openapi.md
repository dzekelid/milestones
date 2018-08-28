---
swagger: "2.0"
x-collection-name: GitLab
x-complete: 0
info:
  title: GitLab Get Projects Milestones
  version: 1.0.0
  description: Get a list of project milestones
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