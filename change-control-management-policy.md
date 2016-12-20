# Change Management/Control Process (12.1.2)

Changes are made to the information technology systems in a _seven_-step process.

> The _complete_ detail for this process is described in the "Contributing" Guide:
https://github.com/dwyl/contributing

## 1. Change Initiator Identifies Feature Requirement (Need for Change)

The requirement for a change or new feature can be initiated by "the business"
or an end-user; the "change initiator". The requirement is captured in the
shared "backlog" (GitHub issues) with as much detail as possible.

> Preferably the requirement should be described in the form of
a "user story" or "bug report" to ensure adequate detail is captured.

_Occasionally_ an opportunity for change/improvement will be identified by a member
development team. In this case at least one other member of the team must
confirm the opportunity for change/improvement has business/user value before
it can proceed to prioritisation.


## 2. Confirmation of Need & Requirement from Stakeholders

Once the change/feature/bug has been identified and described (_in step 1_)
we require _confirmation_ from at least one _other_ stakeholder.
This is to ensure that non-essential changes cannot be made on a whim.


## 3. Work Prioritisation

All features are prioritized by "product owner" (_or "the business" / management team_)


## 4. Change Performed by Technical Team

The work of building the feature or preparing the change is performed by a
member of the development team.

### Developer Checklist

+ [ ] Unit, End-to-End and/or Acceptance Test is written
+ [ ] Feature/change is built according to precise requirements and no other additions/removals made.
+ [ ] Descriptive Git Commit Message with reference (link) to issue.
+ [ ] Ensure all `pre-commit` checks/tests pass locally before pusing to Continuous Integration (CI) Environment.
+ [ ] Push to CI
+ [ ] Create "Pull Request" (_with batch of changes_)
+ [ ] Assign for request for peer review.

## 5. Peer Review

The code is reviewed by peers (_a distinct team member_) and improvements suggested.
When code is deemed good approval is given.

## 6. Quality Assurance Review

QA reviews the change and either requests changes or approves and merges.

## 7. Release to Production

Once all preceeding steps are complete
