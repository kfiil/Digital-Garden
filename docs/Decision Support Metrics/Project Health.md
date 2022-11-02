# Project Health

In order to give incentives to improve, the problematic parts needs to be measured and visualized in a good way. This page lists a set of metrics that are used to calculate which level a project is at. It is inspired by Google's old [Test Certified](https://mike-bland.com/2011/10/18/test-certified.html) definition and more recent developments internally at Google.

## Functional requirements

See next section for numbers referred to as X.

* **Level 1:**
  * Have a continuous build executing per commit
  * Measure coverage on automated tests
* **Level 2:**
  * Establishing a written policy that essentially forbids anyone from submitting untested code
  * Require X% test coverage
  * Max X static analysis errors
  * Max execution time of all tests \(with code coverage enabled\)
* **Level 3:**
  * Stricter limits of above metrics
  * Minimum release frequency to production
* **Level 4-5:**
  * Stricter limits of above metrics

**Notice:** All criterias must be met to grade a project at a specific level. As soon one metric goes below, the level is reduced.

## Numerical requirements

| **Level** | **Test coverage** | **Test execution time \(all tests\)** | **SonarQube violations score \(weighted\)** | **Release frequency \(to prod\)** | **Release window allowed** |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | &gt;=40% | &lt;=60 min | 2000 | - | - |
| 2 | &gt;=50% | &lt;=20min | 1000 | - | 02.00 - 05.00 CET |
| 3 | &gt;=60% | &lt;=15min | 500 | &lt;=1 month | 02.00 - 05.00 CET |
| 4 | &gt;=70% | &lt;=10min | 200 | &lt;=2 weeks | 02.00 - 05.00 CET, 06.00 - 08.00 CET, 14.00 - 16.00 CET |
| 5 | &gt;=80% | &lt;=5min | 100 | &lt;=1 week | 02.00 - 05.00 CET, 06.00 - 08.00 CET, 14.00 - 16.00 CET |

## SonarQube violations score

In order to give incentives for fixing the more serious violations and to account for project size, the following formula is used for SonarQube violation points:

score = \(50 \* blockers + 20 \* critical + 5 \* major + 1 \* minor + 0.5 \* info\) / \(NLOC/1000\)

**Example** :

A project with 2000 lines of code with 3 blocker, 4 critical and 10 minor violations would get a score of \(50\*3+20\*4+1\*10\) / \(2000/1000\) = 120 points. If the project only had 1000 lines of code, the score would be twice as high: 240.

## Potential future metrics

* **Release branch cherry-picking:** to measure the number of cherry-picks/hotfixes that are made to production releases \(i.e. patch releases\). This depends on that release branches are cut from master and that cherry-picking takes place onto such branches for hotfixes. This is not the current release managment stategy for most projects, so it needs more work to be applicable.
* **Categorizing tests** as "unit", "integration" or "end-to-end" and have individual coverage requirements on each. There's one downside with this however - it gives incentives of writing too many integration and end-to-end tests, which changes the test balance away from the desired one, which should be according to the "Test Pyramid": ![Testing pyramid 2.0](https://static.wixstatic.com/media/7a4f4d_c467718df89d4d60b83f0ebcfb81178c~mv2.jpg/v1/fill/w_1000,h_916,al_c,q_90,usm_0.66_1.00_0.01/7a4f4d_c467718df89d4d60b83f0ebcfb81178c~mv2.jpg)
* **Incremental test coverage** : to measure coverage per Pull request, to ensure new code is tested. If the infrastructure can provide this number, this test coverage requirement should be higher than the total absolute coverage for a project.
* **Test flakiness** : to have a maximum allowed % of flaky tests \(tests that fails sometimes, due to timing issues, poorly written code, network timeouts, etc\) in each build. This requires an investment in infrastructure tooling in order to be possible to collect.

