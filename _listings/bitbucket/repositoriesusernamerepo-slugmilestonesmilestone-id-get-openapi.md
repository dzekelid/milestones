---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Get Repositories Username Repo Slug Milestones Milestone
  description: Get repositories username repo slug milestones milestone
  termsOfService: https://www.atlassian.com/legal/customer-agreement
  contact:
    name: Bitbucket Support
    url: https://support.atlassian.com/bitbucket
    email: support@bitbucket.org
  version: 1.0.0
host: api.bitbucket.org
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repositories/{username}/{repo_slug}/milestones:
    get:
      summary: Get Repositories Username Repo Slug Milestones
      description: |-
        Returns the milestones that have been defined in the issue tracker.

        This resource is only available on repositories that have the issue
        tracker enabled.
      operationId: getRepositoriesUsernameRepoSlugMilestones
      x-api-path-slug: repositoriesusernamerepo-slugmilestones-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
    parameters:
      summary: Parameters Repositories Username Repo Slug Milestones
      description: Parameters repositories username repo slug milestones
      operationId: parametersRepositoriesUsernameRepoSlugMilestones
      x-api-path-slug: repositoriesusernamerepo-slugmilestones-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
  /repositories/{username}/{repo_slug}/milestones/{milestone_id}:
    get:
      summary: Get Repositories Username Repo Slug Milestones Milestone
      description: Get repositories username repo slug milestones milestone
      operationId: getRepositoriesUsernameRepoSlugMilestonesMilestone
      x-api-path-slug: repositoriesusernamerepo-slugmilestonesmilestone-id-get
      parameters:
      - in: path
        name: milestone_id
        description: The milestones id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
      - Milestone
    parameters:
      summary: Parameters Repositories Username Repo Slug Milestones Milestone
      description: Parameters repositories username repo slug milestones milestone
      operationId: parametersRepositoriesUsernameRepoSlugMilestonesMilestone
      x-api-path-slug: repositoriesusernamerepo-slugmilestonesmilestone-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
      - Milestone
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