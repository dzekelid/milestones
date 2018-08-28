swagger: "2.0"
x-collection-name: Google Play
x-complete: 1
info:
  title: Google Play
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /quests/{questId}/milestones/{milestoneId}/claim:
    put:
      summary: Claim Quest Milestone
      description: Report that a reward for the milestone corresponding to milestoneId
        for the quest corresponding to questId has been claimed by the currently authorized
        user.
      operationId: games.questMilestones.claim
      x-api-path-slug: questsquestidmilestonesmilestoneidclaim-put
      parameters:
      - in: query
        name: consistencyToken
        description: The last-seen mutation timestamp
      - in: path
        name: milestoneId
        description: The ID of the milestone
      - in: path
        name: questId
        description: The ID of the quest
      - in: query
        name: requestId
        description: A numeric ID to ensure that the request is handled correctly
          across retries
      responses:
        200:
          description: OK
      tags:
      - Milestone