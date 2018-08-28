---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Patch Repos Owner Repo Milestones Number
  description: Update a milestone.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repos/{owner}/{repo}/milestones:
    get:
      summary: Get Repos Owner Repo Milestones
      description: List milestones for a repository.
      operationId: list-milestones-for-a-repository
      x-api-path-slug: reposownerrepomilestones-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: query
        name: direction
        description: Ignored without sort parameter
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      - in: query
        name: sort
      - in: query
        name: state
        description: String to filter by state
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Milestones
    post:
      summary: Add Repos Owner Repo Milestones
      description: Create a milestone.
      operationId: create-a-milestone
      x-api-path-slug: reposownerrepomilestones-post
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Milestones
  /repos/{owner}/{repo}/milestones/{number}:
    delete:
      summary: Delete Repos Owner Repo Milestones Number
      description: Delete a milestone.
      operationId: delete-a-milestone
      x-api-path-slug: reposownerrepomilestonesnumber-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of milestone
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Milestones
      - Number
    get:
      summary: Get Repos Owner Repo Milestones Number
      description: Get a single milestone.
      operationId: get-a-single-milestone
      x-api-path-slug: reposownerrepomilestonesnumber-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: number
        description: Number of milestone
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Milestones
      - Number
    patch:
      summary: Patch Repos Owner Repo Milestones Number
      description: Update a milestone.
      operationId: update-a-milestone
      x-api-path-slug: reposownerrepomilestonesnumber-patch
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: number
        description: Number of milestone
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Milestones
      - Number
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