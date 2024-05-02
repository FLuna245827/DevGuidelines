# DevGuidelines
## Java Developer Guidelines - For getting better quality software

Here are some recommended actions while developing in Java through all the dev cycle.

Notes: We'll consider that the versioning control system being used is Git.

1. Preparation
   * On Git versioning
     * Master branch.
       The master branch shall be kept for having the 'Production' code only.
       No developing shall be done at the master branch.       
     * Master child branches.
       Any required development branches shall be derived from the master branch.
       * Follow a Top-to-Bottom hierarchy is recommended, being obvious at the top the Master branch.
       * The child branches may reflect the way an organisation works, ie. it could be a branch for every team, a branch for a specific application, etc.
       * Other sub-branches may be derived for every developer. For example, a "Team A" branch can be created from the master branch, and then "Developper1", "Developper2"... branches can be derived from the "Team A" one.
       * No developer branch shall be created from the Master one.
       * Any number of developer branches should be at the bottom of the hierarchy.
     * Rebase vs Merge.
         * The *Rebase* action should be used to keep the branch up to date with respect to his parent branch.
         * The *Merge* action should be used to deliver the code to his parent branch.
2. While writing code
   * Add comments specially when a decision was made so to explain the reason of that code.
3. On testing
   * If unit and integration tests are written before coding, this step may be done before step 2 above.
   * Run a code coverage tool.
     * After unit and integrations tests are finished, a code coverage tool can help find what parts of the code still need to be covered by tests.
4. Code delivery
   * Before demanding a Merge Request:
     * Run unit and integration tests. All tests that are included in the code to be deliver must be executed.
     * Detect and correct issues. Run external tools like SonarLint and fix most quality issues.

### When developping microservices
* Document the service contract with OpenAPI, to let know what and how the inputs and outputs are expected.
     
