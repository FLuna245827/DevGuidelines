# DevGuidelines
Java Developer Guidelines

Here are some recommended actions while developing in Java through all the dev cycle.
Notes: It's considered here that the versioning control system being used is Git.

1) Preparation
   On Git versioning
     Master branch.
       The master branch shall be kept for having the 'Production' code only.
       No developing shall be done at the master branch.       
     Master children branches.
       Any required development branches shall be derived from the master branch.
       Follow a Top-to-Bottom hierarchy is recommended, being obvious at the top the Master branch.
       The child branches may reflect the way an organisation works, ie. it could be a branch for every team, a branch for a specific application, etc.
       Other sub-branches may be derived for every developer. For example, a "Team A" branch can be created from the master branch, and then "Developper1", "Developper2"... branches can be derived from the "Team A" one.
       No developer branch shall be created from the Master one.
       Any number of developer branches should be at the bottom of the hierarchy.
     Rebase vs Merge.
       Standing on a branch, a Rebase action should be used to put the branch up to date with respect to his parent, and a Merge action should be used to 'deliver' the code to his parent branch.
3) While writing code
   
4) On testing
   If unit and integration tests are written before coding, this step may be done before step 2 above.
   Run a code coverage tool. After unit and integrations tests are finished, a code coverage tool can help to find what parts of the code still need to be covered by tests.
5) Code delivery
   Before demanding a Merge Request the following actions should be executed:
     Running unit and integration tests. All tests that are included in the code to be deliver must be executed.
     Detect and correct issues. Run external tools like SonarLint and fix most quality issues.
     
