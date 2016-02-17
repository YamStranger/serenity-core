
## # Serenity BDD Core Change Log

### v1.1.26-rc.4
** Commits with examples **
- [bc1a2848e81e56c](https://github.com/serenity-bdd/serenity-core/commit/bc1a2848e81e56c) Refactored some unit tests to check the fix for the Saucelinks link problem properly
- [c80004c26a41faa](https://github.com/serenity-bdd/serenity-core/commit/c80004c26a41faa) Made the Cucumber support more robust
 The parser will no longer crash if there are empty or badly-formed feature files. 
- [7200f4b42c1dc8d](https://github.com/serenity-bdd/serenity-core/commit/7200f4b42c1dc8d) Minor bug fix with the Saucelabs video icon
 Minor bug fix where the Saucelabs video icon was incorrectly displayed. 
### v1.1.26-rc.3
** Commits with examples **
- [433b732734f4eaa](https://github.com/serenity-bdd/serenity-core/commit/433b732734f4eaa) Allow more elegant waits in the Screenplay module
 You can now write code like this: 
 jane.should(eventually(seeThat(TheClickerValue.of(clicker), equalTo(10)))) 
 This will not fail if the matcher cannot be evaluated the first time, but will retry up to a maximum of &#39;serenity.timouts&#39; seconds (5 by default). 
- [e0c22637eccbd6e](https://github.com/serenity-bdd/serenity-core/commit/e0c22637eccbd6e) Corrected an error in the module names
### v1.1.26-rc.2
** Commits with examples **
- [0e08c8c86f76f9c](https://github.com/serenity-bdd/serenity-core/commit/0e08c8c86f76f9c) Use the correct name for the screenplay library for this version
- [9d5fb9e53e2a7c7](https://github.com/serenity-bdd/serenity-core/commit/9d5fb9e53e2a7c7) style: updating test style
- [91c32382040967d](https://github.com/serenity-bdd/serenity-core/commit/91c32382040967d) fix: updating version of serenityc-core and maven-plugin
- [6f4f5d461d969c0](https://github.com/serenity-bdd/serenity-core/commit/6f4f5d461d969c0) fix: updating logging for serenity gradle plugin, using simple out stream
- [0340f82dcb76e3c](https://github.com/serenity-bdd/serenity-core/commit/0340f82dcb76e3c) fix: updating logging for serenity gradle plugin
- [412657bb56c8740](https://github.com/serenity-bdd/serenity-core/commit/412657bb56c8740) fix: updating gradle plugin to work with new configuration
- [ffdc3efce06074d](https://github.com/serenity-bdd/serenity-core/commit/ffdc3efce06074d) fix: updating requirements directory to be able work with multimodule projects
- [cbc92cba6fc8792](https://github.com/serenity-bdd/serenity-core/commit/cbc92cba6fc8792) fix: updated gradle plugin to work with multimodule projects
- [4f1581ce6369aaa](https://github.com/serenity-bdd/serenity-core/commit/4f1581ce6369aaa) fix: updating getSessionId method to get session id without init new webdriver
- [d9c1e6a65a28bb8](https://github.com/serenity-bdd/serenity-core/commit/d9c1e6a65a28bb8) style: updated name of test method
- [bf8fca33efc9aa0](https://github.com/serenity-bdd/serenity-core/commit/bf8fca33efc9aa0) fix: remote driver session id can be under proxied driver
- [909f21a66d8f732](https://github.com/serenity-bdd/serenity-core/commit/909f21a66d8f732) Renamed serenity-journey to serenity-screenplay
 Also allow conditional tasks of the following form: 
 dana.attemptsTo( 
 Check.whether(cost&gt;100) 
 .andIfSo(purchaseAPear) 
 .otherwise(purchaseAnApple) 
 ); 
 Or with a Question&lt;Boolean&gt;: 
 dana.attemptsTo( 
 Check.whether(itIsTooExpensive) 
 .andIfSo(purchaseAPear) 
 .otherwise(purchaseAnApple) 
 ); 
- [720c516a2a126fb](https://github.com/serenity-bdd/serenity-core/commit/720c516a2a126fb) chore: added gitattributes
### v1.1.26-rc.1
** Commits with examples **
- [91aee6a29aae70e](https://github.com/serenity-bdd/serenity-core/commit/91aee6a29aae70e) Revert &quot;Git Attributes Experiment, please don&#39;t merge&quot;
- [0dcba83994ed144](https://github.com/serenity-bdd/serenity-core/commit/0dcba83994ed144) Revert &quot;Updating gitattributes not to update chromedriver and woff files&quot;
- [e71056d57767f35](https://github.com/serenity-bdd/serenity-core/commit/e71056d57767f35) fix: updated gitattributes
- [b98f19f058c8035](https://github.com/serenity-bdd/serenity-core/commit/b98f19f058c8035) chore: updated gitattributes
- [5236c58bf846648](https://github.com/serenity-bdd/serenity-core/commit/5236c58bf846648) Revert &quot;Git Attributes Experiment, please don&#39;t merge&quot;
- [c6122c8a4976149](https://github.com/serenity-bdd/serenity-core/commit/c6122c8a4976149) fix: fixed nullpointer if json config does not exists
- [862b790b16d85ac](https://github.com/serenity-bdd/serenity-core/commit/862b790b16d85ac) Updated smoke tests
- [612401d19781815](https://github.com/serenity-bdd/serenity-core/commit/612401d19781815) Minor refactoring
- [c9572c849d9e710](https://github.com/serenity-bdd/serenity-core/commit/c9572c849d9e710) Actors can now perform tasks conditionally
 Use the Unless class static methods and a bolean expression, e.g. 
 ``` 
 Unless.the(items.isEmpty(), AddTodoItems.called(items)) 
 ``` 
 or use a question of type Question&lt;Boolean&gt;: 
 ``` 
 Unless.the(itemsListisEmpty(), AddTodoItems.called(items)) 
 ``` 
- [3e0d99168dbec1a](https://github.com/serenity-bdd/serenity-core/commit/3e0d99168dbec1a) Actors can now perform tasks conditionally
 Use the Unless class static methods and a bolean expression, e.g. 
 ``` 
 Unless.the(items.isEmpty(), AddTodoItems.called(items)) 
 ``` 
 or use a question of type Question&lt;Boolean&gt;: 
 ``` 
 Unless.the(itemsListisEmpty(), AddTodoItems.called(items)) 
 ``` 
### v1.1.25-rc.7
** Commits with examples **
- [5cb49b2e6ce64c5](https://github.com/serenity-bdd/serenity-core/commit/5cb49b2e6ce64c5) Made reading UI values more fluent.
 The narrative was interrupted by the .value() so hidden away for now behind a more fluent method 
- [c28a95ec9310748](https://github.com/serenity-bdd/serenity-core/commit/c28a95ec9310748) Support for multiple matchers in Consequences
 You can now make multiple assertions against a single question 
- [ea5f1adc05581fc](https://github.com/serenity-bdd/serenity-core/commit/ea5f1adc05581fc) fix: restored gitattributes
### v1.1.25-rc.6
** Commits with examples **
- [4b1537ede322502](https://github.com/serenity-bdd/serenity-core/commit/4b1537ede322502) Restored a renamed method to maintain backward compatibility.
- [9e66e4bd6f59659](https://github.com/serenity-bdd/serenity-core/commit/9e66e4bd6f59659) fix: updated commons-collection for jira/jbehave/cucumber modules
### v1.1.25-rc.5
** Commits with examples **
- [c4a8fc16ec943ca](https://github.com/serenity-bdd/serenity-core/commit/c4a8fc16ec943ca) Refactoring and performance improvements
- [2e2450a32770d5e](https://github.com/serenity-bdd/serenity-core/commit/2e2450a32770d5e) Tests can now manage whether cookies should be cleared between each test
### v1.1.25-rc.4
** Commits with examples **
- [0a9e50ae5782ba9](https://github.com/serenity-bdd/serenity-core/commit/0a9e50ae5782ba9) Fixed #255
- [95449fed05268e1](https://github.com/serenity-bdd/serenity-core/commit/95449fed05268e1) style: update test style
- [3e864ae7bfeef59](https://github.com/serenity-bdd/serenity-core/commit/3e864ae7bfeef59) fix: selenium version upgrade to 2.50.1
- [4e495f56444915a](https://github.com/serenity-bdd/serenity-core/commit/4e495f56444915a) style: test updated
- [194f3d966d78014](https://github.com/serenity-bdd/serenity-core/commit/194f3d966d78014) fix: updated report template generation
- [85e23de89036021](https://github.com/serenity-bdd/serenity-core/commit/85e23de89036021) fix: update charset usage during reading/writing
- [ba8fcee2574ce65](https://github.com/serenity-bdd/serenity-core/commit/ba8fcee2574ce65) Hardened some of the integration tests
- [4858e0b156973d1](https://github.com/serenity-bdd/serenity-core/commit/4858e0b156973d1) fix: updating report engine to wait results of report generation, stream and readers closing
- [e772cd1b4d1773d](https://github.com/serenity-bdd/serenity-core/commit/e772cd1b4d1773d) Attempt to make some of the tests more robust.
- [1b3aa6568c4a004](https://github.com/serenity-bdd/serenity-core/commit/1b3aa6568c4a004) Removed the .gitattribues file from git as it causes problems with the build pipeline on Snap-CI
- [4531d43df845228](https://github.com/serenity-bdd/serenity-core/commit/4531d43df845228) Fixed issue #281
 During verbose logging, Serenity tried to read the tag from web elements. This could cause failures if the element was stale or unavailable when the logging happen. This has now been changed to log the locator and not the element tag type. 
- [9f1f6b5c05f6c1b](https://github.com/serenity-bdd/serenity-core/commit/9f1f6b5c05f6c1b) Added an Action class to scroll to a particular eleemtn on the screen.
- [123e26d0bda8d05](https://github.com/serenity-bdd/serenity-core/commit/123e26d0bda8d05) fix: updated processing of &quot;browserstack.os.version&quot; and &quot;browserstack.browser.version&quot; system properties according to latest changes on BrowserStack side
- [e96d512758d1846](https://github.com/serenity-bdd/serenity-core/commit/e96d512758d1846) style: updated test
- [9eb93903d47414a](https://github.com/serenity-bdd/serenity-core/commit/9eb93903d47414a) chore: updating gitignore
- [737b1aaf46a94ab](https://github.com/serenity-bdd/serenity-core/commit/737b1aaf46a94ab) chore: updated wrapper, and build publishing libs
- [55b06c1ce3ecc50](https://github.com/serenity-bdd/serenity-core/commit/55b06c1ce3ecc50) chore: updated wrapper, and build publishing libs
- [9429532576a50ad](https://github.com/serenity-bdd/serenity-core/commit/9429532576a50ad) Moving definition of reportDirectory in order to allow easy configuration through the serenity block. Currently this directory gets set when applying the plugin, which makes it only possible to change through setting an environment variable at the same level as applying the plugin. For multi-module projects with compile dependencies, this does not work
- [ed33d6a045ffeed](https://github.com/serenity-bdd/serenity-core/commit/ed33d6a045ffeed) Updated to Seleniy, 2.49.1
### v1.1.25-rc.3
** Commits with examples **
- [adc66f3bd6142af](https://github.com/serenity-bdd/serenity-core/commit/adc66f3bd6142af) added a test to check the test report output; updated previously failed tests for customized step title
- [af3562dcf668650](https://github.com/serenity-bdd/serenity-core/commit/af3562dcf668650) updated existing tests after changes in ExecutedStepDescription class
- [e25d54860c48130](https://github.com/serenity-bdd/serenity-core/commit/e25d54860c48130) added the tests to cover storing arguments list in ExecutedStepDescription class
- [9d046220442e6d6](https://github.com/serenity-bdd/serenity-core/commit/9d046220442e6d6) fix: customized step title if some parameter contains comma character
- [864c00c9d01ce7b](https://github.com/serenity-bdd/serenity-core/commit/864c00c9d01ce7b) delted maven repo from build.gradle
- [42be3ba710578c2](https://github.com/serenity-bdd/serenity-core/commit/42be3ba710578c2) Browsermob update: using browsermob-core-littleproxy instead of old browsermob-proxy
- [c9c9e1b8a682ba3](https://github.com/serenity-bdd/serenity-core/commit/c9c9e1b8a682ba3) chore: turn off parallel execution of submodules
- [12b5943d2f74407](https://github.com/serenity-bdd/serenity-core/commit/12b5943d2f74407) chore: updated org.gradle.workers.max value to reduce memory usage during build
- [9d6e27dcb4f231d](https://github.com/serenity-bdd/serenity-core/commit/9d6e27dcb4f231d) chore: updated org.gradle.workers.max value to reduce memory usage during build
- [418d37ca898fe72](https://github.com/serenity-bdd/serenity-core/commit/418d37ca898fe72) chore: updated org.gradle.workers.max value to reduce memory usage during build
- [0a8a1856c6c06b9](https://github.com/serenity-bdd/serenity-core/commit/0a8a1856c6c06b9) chore: updated build to enable paralell build
- [f973f15b6c89d2e](https://github.com/serenity-bdd/serenity-core/commit/f973f15b6c89d2e) fix: updated plugin to get serenity.properties from current module build dir
- [246246020826f03](https://github.com/serenity-bdd/serenity-core/commit/246246020826f03) fix: updated build task dependecies
- [530450bb5c94b71](https://github.com/serenity-bdd/serenity-core/commit/530450bb5c94b71) fix: updated resolution of output dir based on gradle/maven module
- [89eebf56d85309e](https://github.com/serenity-bdd/serenity-core/commit/89eebf56d85309e) fix: serenity.properties can be located not in workin dir, but in gradle/maven module folder
- [c47b69d154d32aa](https://github.com/serenity-bdd/serenity-core/commit/c47b69d154d32aa) chore: build test parallel execution enabled (PerCore)
- [36225a5908e8b2c](https://github.com/serenity-bdd/serenity-core/commit/36225a5908e8b2c) fix: report generation for multimodule builds
- [60b1b99079044a0](https://github.com/serenity-bdd/serenity-core/commit/60b1b99079044a0) Fine-tuned the soft-assert tests and minor reporting bug  fix.
### v1.1.25-rc.2
** Commits with examples **
- [511f6079b8eb17d](https://github.com/serenity-bdd/serenity-core/commit/511f6079b8eb17d) Added support for By locators in Target objects and Action classes.
- [e2ea2ea4999fe72](https://github.com/serenity-bdd/serenity-core/commit/e2ea2ea4999fe72) Updated smoketests
- [2b2d49d1ac787ac](https://github.com/serenity-bdd/serenity-core/commit/2b2d49d1ac787ac) Added support for By locators in Target objects and Action classes.
### v1.1.25-rc.1
** Commits with examples **
- [1f0dba14b3c4c55](https://github.com/serenity-bdd/serenity-core/commit/1f0dba14b3c4c55) Updated smoke test dependencies
- [7caec064fd2d81d](https://github.com/serenity-bdd/serenity-core/commit/7caec064fd2d81d) Removed a redundant test
- [c7bcd9643a1d3b7](https://github.com/serenity-bdd/serenity-core/commit/c7bcd9643a1d3b7) Multiple assertions in the same should() method are now treated as &quot;soft&quot; asserts.
- [05ac6bd4c911b89](https://github.com/serenity-bdd/serenity-core/commit/05ac6bd4c911b89) Revert &quot;#243 Upgrading typesafe.config from 1.2 to 1.3&quot;
- [5f78a7b2ca9d63e](https://github.com/serenity-bdd/serenity-core/commit/5f78a7b2ca9d63e) style: changed style of one test
- [5db32dfbc9fba66](https://github.com/serenity-bdd/serenity-core/commit/5db32dfbc9fba66) fix: update serenity-gradle-plugin to use same Configuration as Tests
- [a610239496c0955](https://github.com/serenity-bdd/serenity-core/commit/a610239496c0955) fix: aggregation report generation in gradle plugin
- [b944867051253bd](https://github.com/serenity-bdd/serenity-core/commit/b944867051253bd) chore: upgrade groovy from 2.3.* to 2.4.4
- [a60d52606dfc710](https://github.com/serenity-bdd/serenity-core/commit/a60d52606dfc710) fix: move reports about configuration to specific folder
- [5d17bd44a9869b0](https://github.com/serenity-bdd/serenity-core/commit/5d17bd44a9869b0) chore: gradle take version from local variable
- [d5b5401f3adfc8f](https://github.com/serenity-bdd/serenity-core/commit/d5b5401f3adfc8f) chore: gradle to 2.10 and groovy to 2.4.4 upgraded
- [777c06110da4f2a](https://github.com/serenity-bdd/serenity-core/commit/777c06110da4f2a) fix: report with properties should be in json
- [9e412bfeb9d5839](https://github.com/serenity-bdd/serenity-core/commit/9e412bfeb9d5839) fix: report with properties should be in report folder
- [8efe039bbb25754](https://github.com/serenity-bdd/serenity-core/commit/8efe039bbb25754) chore: added report for configuration, with actual properties
### v1.1.24
** Commits with examples **
- [32aba8a8a1676a7](https://github.com/serenity-bdd/serenity-core/commit/32aba8a8a1676a7) Improved exception reporting
- [b5a6c975fb31e82](https://github.com/serenity-bdd/serenity-core/commit/b5a6c975fb31e82) Improved exception reporting
- [f36115c4978f460](https://github.com/serenity-bdd/serenity-core/commit/f36115c4978f460) Added matchers to allow questions about web element states (designed mainly to be used for low-level preconditions or assertions), e.g.
 then(dana).should(seeThat(the(ProfilePage.NAME_FIELD), isVisible())); 
- [198a036ac2e3ce4](https://github.com/serenity-bdd/serenity-core/commit/198a036ac2e3ce4) Improved reporting of customised error messages in consequences
- [1dbda1aec900a98](https://github.com/serenity-bdd/serenity-core/commit/1dbda1aec900a98) docs: adding instructions of contributors
- [e240e7f100216a1](https://github.com/serenity-bdd/serenity-core/commit/e240e7f100216a1) chore: upgrade typesafe.config to 1.3 from 1.2
### v1.1.22-rc.15
** Commits with examples **
- [8d6dafa79e3917e](https://github.com/serenity-bdd/serenity-core/commit/8d6dafa79e3917e) Fixed a bug in the reporting of Journey Pattern web actions.
- [594460938c80423](https://github.com/serenity-bdd/serenity-core/commit/594460938c80423) When using a unique browser for multiple tests, clear the cookies and HTML local storage between tests.
- [c200b3262d83a1d](https://github.com/serenity-bdd/serenity-core/commit/c200b3262d83a1d) Improved the reporting of Journey pattern by removing redundant &quot;is&quot; clauses generated by the Hamcrest matchers.
### v1.1.22-rc.14
** Commits with examples **
- [b6586774ee26b6e](https://github.com/serenity-bdd/serenity-core/commit/b6586774ee26b6e) Added the Evaluate action and the JavaScript question to perform JavaScript queries.
- [ef0e61af836455a](https://github.com/serenity-bdd/serenity-core/commit/ef0e61af836455a) Updated the smoke tests.
- [a700aa2d0654491](https://github.com/serenity-bdd/serenity-core/commit/a700aa2d0654491) The Target class now accepts a prefix notation to specify the locator, e.g Target.the(&quot;name field&quot;).locatedBy(&quot;css:#name&quot;) or Target.the(&quot;name field&quot;).locatedBy(&quot;id:name&quot;)
 This supports all of the WebDriver locator strategies: 
 - id 
 - css 
 - xpath 
 - name 
 - tagName 
 - className 
 - linkText 
 - partialLinkText 
- [e8d86a9b1562f22](https://github.com/serenity-bdd/serenity-core/commit/e8d86a9b1562f22) Refactored a journey pattern test to illustrate the displays matcher
- [182dfa03c9c217c](https://github.com/serenity-bdd/serenity-core/commit/182dfa03c9c217c) Refactored the Journey Pattern code
- [e9610ed6fc8e761](https://github.com/serenity-bdd/serenity-core/commit/e9610ed6fc8e761) Refactored the Enter action to allow entering text and keys in the same action
### v1.1.22-rc.13
** Commits with examples **
- [7e41d67d6acaf5d](https://github.com/serenity-bdd/serenity-core/commit/7e41d67d6acaf5d) Trying to fixe a performance issue related to resource copying
- [00615130588c8b2](https://github.com/serenity-bdd/serenity-core/commit/00615130588c8b2) Added a method to the WebDriverManager instance to retreive a named webdriver instance.
- [eec89ad0c6d2488](https://github.com/serenity-bdd/serenity-core/commit/eec89ad0c6d2488) Fixed a bug that reported a misleading &quot;class cast exception&quot; when the moveTo() method was called after a test failure.
- [8dad9ccfa05c76e](https://github.com/serenity-bdd/serenity-core/commit/8dad9ccfa05c76e) Added the ability to use the Serenity WebDriver API directly in Action classes, by extending the WebAction class.
- [5fdf07c2b07a731](https://github.com/serenity-bdd/serenity-core/commit/5fdf07c2b07a731) Fixed a bug where enums did not appear correctly in the test reports when they were referenced by Journey Pattern Questions.
- [edcdc4ad932fc62](https://github.com/serenity-bdd/serenity-core/commit/edcdc4ad932fc62) It is now possible to add page objects as member variables in Performable or Question classes - they will be correctly configured with the WebDriver instance associated with the actor.
- [c8261771133d28e](https://github.com/serenity-bdd/serenity-core/commit/c8261771133d28e) Refactored the bundled Journey Pattern action classes.
### v1.1.22-rc.12
** Commits with examples **
- [32282fee3f80aaf](https://github.com/serenity-bdd/serenity-core/commit/32282fee3f80aaf) Updated smoketests to refactored journey pattern
- [c6803e834640e9d](https://github.com/serenity-bdd/serenity-core/commit/c6803e834640e9d) Readability improvements and moved the UI Action classes into their own package.
- [4c9a1b1ec71d248](https://github.com/serenity-bdd/serenity-core/commit/4c9a1b1ec71d248) 223_issue: reloading result dir
- [8d42d0d2f40dea5](https://github.com/serenity-bdd/serenity-core/commit/8d42d0d2f40dea5) 223_issue: reverting updating of some imports
- [994da12a7d2a331](https://github.com/serenity-bdd/serenity-core/commit/994da12a7d2a331) Revert &quot;Pull request for updating SerenityRest to log all types of input&quot;
- [54721c4a11479df](https://github.com/serenity-bdd/serenity-core/commit/54721c4a11479df) 223_issue: added reloading output dir for tests
- [c46729fb285850d](https://github.com/serenity-bdd/serenity-core/commit/c46729fb285850d) 217_issue: style fix
- [9c8f3b20036cdb6](https://github.com/serenity-bdd/serenity-core/commit/9c8f3b20036cdb6) 217_issue: removed dependency org.mortbay.jetty:servlet-api-2.5:6.1.9, it is duplicated with javax.servlet:javax.servlet-api:3.1.0
- [0e4b788b99f6a3a](https://github.com/serenity-bdd/serenity-core/commit/0e4b788b99f6a3a) 217_issue: removed old and never updated files
### v1.1.22-rc.11
** Commits with examples **
- [86ff95a0f343746](https://github.com/serenity-bdd/serenity-core/commit/86ff95a0f343746) 216_issue: update versions
- [c44f078c170cb79](https://github.com/serenity-bdd/serenity-core/commit/c44f078c170cb79) 218_issue: added test for checking if web scenarious executed successfully with HTMLUnit (fails now, so added @Ignore)
- [5f8752f8da66e0b](https://github.com/serenity-bdd/serenity-core/commit/5f8752f8da66e0b) 216_issue: update versions
- [f998b4a55e25fe8](https://github.com/serenity-bdd/serenity-core/commit/f998b4a55e25fe8) 185_issue: log and auth wrappers implemented, tests profivided. redirects still not supported
- [7ab6c2502ff35f1](https://github.com/serenity-bdd/serenity-core/commit/7ab6c2502ff35f1) 197_issue: updated SerenityRest to log all types of input for content/body rest call
- [2cec6f26c6f2f87](https://github.com/serenity-bdd/serenity-core/commit/2cec6f26c6f2f87) fix: Fix for setting serenity.proxy.type and http_port. Needs to be an number instead of string.
- [7c4e0df97b5bb04](https://github.com/serenity-bdd/serenity-core/commit/7c4e0df97b5bb04) fix: cglib dependency conflict from guice
### v1.1.22-rc.10
** Commits with examples **
- [e21e9a5c18b2e3c](https://github.com/serenity-bdd/serenity-core/commit/e21e9a5c18b2e3c) Updated tests
- [9f9075212fc2f3c](https://github.com/serenity-bdd/serenity-core/commit/9f9075212fc2f3c) Retry to unzip a resource file if it is locked. This is a work-around for Windows-related file locking issues.
- [81c87bb9040cacb](https://github.com/serenity-bdd/serenity-core/commit/81c87bb9040cacb) Fixed an error with the screenshots that always displayed the screen source link, even for successful tests.
- [fc8442b03447e52](https://github.com/serenity-bdd/serenity-core/commit/fc8442b03447e52) Restored step logging to INFO.
- [c9889ca6204e9a5](https://github.com/serenity-bdd/serenity-core/commit/c9889ca6204e9a5) Added more robustness to the report generation by allowing ZIP files to be opened again if they couldn&#39;t the first time
### v1.1.22-rc.9
** Commits with examples **
- [930f34cb355c189](https://github.com/serenity-bdd/serenity-core/commit/930f34cb355c189) Record screen source code for failing tests.
- [73015c29b297366](https://github.com/serenity-bdd/serenity-core/commit/73015c29b297366) fix for nested cleaning resources
- [8d03dda6b41d7f3](https://github.com/serenity-bdd/serenity-core/commit/8d03dda6b41d7f3) Updated tests for screenshots
- [4267bd936dc4dc3](https://github.com/serenity-bdd/serenity-core/commit/4267bd936dc4dc3) updated Resizer. Fixed opening output and input stream in same time
- [a7bdaeb08399244](https://github.com/serenity-bdd/serenity-core/commit/a7bdaeb08399244) Updated input streams closing
- [79d266003d25a27](https://github.com/serenity-bdd/serenity-core/commit/79d266003d25a27) see https://github.com/serenity-bdd/serenity-core/issues/179
- [7ebca229c0a391d](https://github.com/serenity-bdd/serenity-core/commit/7ebca229c0a391d) 184_issue: test added
- [b5e520997b94138](https://github.com/serenity-bdd/serenity-core/commit/b5e520997b94138) 184_issue: logging for PATCH operation added
### v1.1.22-rc.8
** Commits with examples **
- [552172c80ce7608](https://github.com/serenity-bdd/serenity-core/commit/552172c80ce7608) Set the serenity.console.colors property to true to get ANSI colors in the console output (don&#39;t use on Jenkins).
### v1.1.22-rc.7
** Commits with examples **
- [d4791cdd90311c5](https://github.com/serenity-bdd/serenity-core/commit/d4791cdd90311c5) Fixed a bug that prevented @Pending annotations from working with non-instrumented Performable objects
### v1.1.22-rc.6
** Commits with examples **
- [283093853e20adf](https://github.com/serenity-bdd/serenity-core/commit/283093853e20adf) Made the console logging colors a bit lighter for better readability
- [e7d7c85df2489c1](https://github.com/serenity-bdd/serenity-core/commit/e7d7c85df2489c1) Updated unit tests
- [5099debaaa78053](https://github.com/serenity-bdd/serenity-core/commit/5099debaaa78053) Added color to logs
- [93b1411da124872](https://github.com/serenity-bdd/serenity-core/commit/93b1411da124872) Added color to logs
- [8846f6e32637978](https://github.com/serenity-bdd/serenity-core/commit/8846f6e32637978) Improved console log messages to cater for errors and failed assumptions
- [e329275237f7aa4](https://github.com/serenity-bdd/serenity-core/commit/e329275237f7aa4) Updated unit tests
- [8a21a9f2ca827b9](https://github.com/serenity-bdd/serenity-core/commit/8a21a9f2ca827b9) Improved reporting
- [4f189ca2db7b989](https://github.com/serenity-bdd/serenity-core/commit/4f189ca2db7b989) 188_issue: new level of take screenshots configuration added
- [42691e1efb02790](https://github.com/serenity-bdd/serenity-core/commit/42691e1efb02790) Improved reporting
- [597960b30fe36a4](https://github.com/serenity-bdd/serenity-core/commit/597960b30fe36a4) Minor Base Step Listener Constructor update
- [1af09f3f475ab89](https://github.com/serenity-bdd/serenity-core/commit/1af09f3f475ab89) 179_issue: added tests and fix for issue
- [5b77f9ac5c51742](https://github.com/serenity-bdd/serenity-core/commit/5b77f9ac5c51742) Photographer cleanup fix. If driver not initialized - nothing to clean
- [ece74d2b38035f3](https://github.com/serenity-bdd/serenity-core/commit/ece74d2b38035f3) Remove an unnecessary moveTo() operation.
 This seems to cause class cast exceptions from time to time. 
- [2d39575adf3fa35](https://github.com/serenity-bdd/serenity-core/commit/2d39575adf3fa35) 130_issue: added system configuration for output dirrectory
- [ef3ca8d84926738](https://github.com/serenity-bdd/serenity-core/commit/ef3ca8d84926738) 130_issue: added system environment properties to configuration
- [bc6e1f9ea2d8fd3](https://github.com/serenity-bdd/serenity-core/commit/bc6e1f9ea2d8fd3) Reduce noise in the logs by removing an superfluous error message.
- [0a1679f36c02583](https://github.com/serenity-bdd/serenity-core/commit/0a1679f36c02583) fix build fail by updating test-outcomes.ftl
- [26219f70f9f5905](https://github.com/serenity-bdd/serenity-core/commit/26219f70f9f5905) 130_issue: reading serenity.properties fix
### v1.1.22-rc.4
** Commits with examples **
- [4c20cd5f39da75b](https://github.com/serenity-bdd/serenity-core/commit/4c20cd5f39da75b) Minor improvement to assertion reporting, to avoid lines being hidden for some assertions
### v1.1.22-rc.3
** Commits with examples **
- [8edf62c3dcbf93a](https://github.com/serenity-bdd/serenity-core/commit/8edf62c3dcbf93a) Better handling of reporting arbitrary AssertionError exceptions.
### v1.1.22-rc.2
** Commits with examples **
- [9bcc6643ff58626](https://github.com/serenity-bdd/serenity-core/commit/9bcc6643ff58626) Better formatting for the result line at the bottom of the test outcome table
- [a241bd85dac63aa](https://github.com/serenity-bdd/serenity-core/commit/a241bd85dac63aa) Test hardening
- [83496ffda0d8e41](https://github.com/serenity-bdd/serenity-core/commit/83496ffda0d8e41) Fine-tuned reporting
- [eb37b9b1589c016](https://github.com/serenity-bdd/serenity-core/commit/eb37b9b1589c016) 132_issue: desabling retries in smoke-tests
- [6ccd53e78491ebb](https://github.com/serenity-bdd/serenity-core/commit/6ccd53e78491ebb) Fixed #175
- [f3e533f87c0a853](https://github.com/serenity-bdd/serenity-core/commit/f3e533f87c0a853) 128_issue: fixing style
- [3eba4e88493fffc](https://github.com/serenity-bdd/serenity-core/commit/3eba4e88493fffc) 128_issue: updated checking Content Type according RFC1341, and added test for https rest tests based on github
- [8a671ce7f4640e4](https://github.com/serenity-bdd/serenity-core/commit/8a671ce7f4640e4) 132_issue: clean task fix
- [02b260e4116e90d](https://github.com/serenity-bdd/serenity-core/commit/02b260e4116e90d) 132_issue: fixing incorrect test. Notifier should record failure
- [632b09d0fb3388f](https://github.com/serenity-bdd/serenity-core/commit/632b09d0fb3388f) 132_issue: little refactoring, moving string to constants
- [dc809646f130397](https://github.com/serenity-bdd/serenity-core/commit/dc809646f130397) 132_issue: updated SerenityRunner to use max.retries only if junit.retry.tests=true, fixing tests from different modules
- [1dae0a507294270](https://github.com/serenity-bdd/serenity-core/commit/1dae0a507294270) 132_issue: updated SerenityRunner to use max.retries only if junit.retry.tests=true, removing description creating method
- [a798480e4e89951](https://github.com/serenity-bdd/serenity-core/commit/a798480e4e89951) 132_issue: updated SerenityRunner to use max.retries only if junit.retry.tests=true, removing imports
- [41361d014bac870](https://github.com/serenity-bdd/serenity-core/commit/41361d014bac870) 132_issue: updated SerenityRunner to use max.retries only if junit.retry.tests=true
- [acf58d8c842dc3f](https://github.com/serenity-bdd/serenity-core/commit/acf58d8c842dc3f) 132_issue: fixing name of menthod in reports
- [27508e1975be3e4](https://github.com/serenity-bdd/serenity-core/commit/27508e1975be3e4) 132_issue: test and solution provided
### v1.1.22-rc.1
** Commits with examples **
- [1b62b2c1e4df337](https://github.com/serenity-bdd/serenity-core/commit/1b62b2c1e4df337) Removed redundant test
- [3e05bb0b83686c9](https://github.com/serenity-bdd/serenity-core/commit/3e05bb0b83686c9) Updated a unit test
- [3794e2b28ed858c](https://github.com/serenity-bdd/serenity-core/commit/3794e2b28ed858c) Improved reporting
 Add the &#39;serenity.linked.tags&#39; property, which allows you to defined tag types which will result in human-readable tags that can be used as bookmarks or external links. 
- [73946ec52a54f9c](https://github.com/serenity-bdd/serenity-core/commit/73946ec52a54f9c) Updated versions in the smoketests
- [7a1c66f46acc6d4](https://github.com/serenity-bdd/serenity-core/commit/7a1c66f46acc6d4) Made the WebdriverManager publicly available for advanced use cases.
### v1.1.21-rc.1
** Commits with examples **
- [4af8b65a5867895](https://github.com/serenity-bdd/serenity-core/commit/4af8b65a5867895) Removed an incorrect reference to a Java 8 class
### v1.1.20-rc.1
** Commits with examples **
- [00d0237227e7f39](https://github.com/serenity-bdd/serenity-core/commit/00d0237227e7f39) Added the &#39;serenity.tag.failures&#39; property, which causes Serenity to add a tag containing the error type for failing tests
- [0e777550299bd00](https://github.com/serenity-bdd/serenity-core/commit/0e777550299bd00) Added the &#39;serenity.tag.failures&#39; property, which causes Serenity to add a tag containing the error type for failing tests
### v1.1.19
** Commits with examples **
- [ba52bc42560b4a0](https://github.com/serenity-bdd/serenity-core/commit/ba52bc42560b4a0) Fixed a potential infinite loop in the report generation if image processing failed for some reason
### v1.1.18-rc.2
** Commits with examples **
- [89a443f17da25d0](https://github.com/serenity-bdd/serenity-core/commit/89a443f17da25d0) Finished merge
- [785c7bedb82ce42](https://github.com/serenity-bdd/serenity-core/commit/785c7bedb82ce42) Finished merge
- [062d4daac873cb0](https://github.com/serenity-bdd/serenity-core/commit/062d4daac873cb0) Improved reporting
- [ca0ffa080140a93](https://github.com/serenity-bdd/serenity-core/commit/ca0ffa080140a93) Fixing getdrivername method to take this.driverClass instead of the getter since the getter may not return a SupportedDriver anymore
- [f6464d1224fd8d5](https://github.com/serenity-bdd/serenity-core/commit/f6464d1224fd8d5) updating tests for using ThucydesWebDriverSupport
- [dcab9c63c6952de](https://github.com/serenity-bdd/serenity-core/commit/dcab9c63c6952de) updating test to use ThucydidesWebDriverSupport
- [b4bbc317f98a23a](https://github.com/serenity-bdd/serenity-core/commit/b4bbc317f98a23a) 130_issue: removing unused dependencies
- [e28f899a152e798](https://github.com/serenity-bdd/serenity-core/commit/e28f899a152e798) 130_issue: fixing copying jars bug
 Conflicts: 
 serenity-gradle-plugin/build.gradle 
- [d2c156debf5b8d1](https://github.com/serenity-bdd/serenity-core/commit/d2c156debf5b8d1) 130_issue: removed emtpy lines
- [920e4cf20364baa](https://github.com/serenity-bdd/serenity-core/commit/920e4cf20364baa) 130_issue: fixed.  Added sample projects for testing serenity-gradle-plugin
- [59a3cb2a96f7a39](https://github.com/serenity-bdd/serenity-core/commit/59a3cb2a96f7a39) 130_issue: spelling error fix
- [60b4922421276c5](https://github.com/serenity-bdd/serenity-core/commit/60b4922421276c5) 130_issue: build.config updated for simple project for serenity-gradle_plugin
- [af55a048e07a081](https://github.com/serenity-bdd/serenity-core/commit/af55a048e07a081) 130_issue: updated simple-gradle-project for serenity-gradle-plugin
- [0d48d61cf44cc34](https://github.com/serenity-bdd/serenity-core/commit/0d48d61cf44cc34) 130_issue: updated simple-gradle-project for serenity-gradle-plugin
- [356fbb9f80c6789](https://github.com/serenity-bdd/serenity-core/commit/356fbb9f80c6789) 130_issue: added test and default project for gradle plugin
### v1.1.18-rc.1
** Commits with examples **
- [6e91a31d3426c4d](https://github.com/serenity-bdd/serenity-core/commit/6e91a31d3426c4d) Revert &quot;Merge branch &#39;master&#39; of github.com:serenity-bdd/serenity-core&quot;
 This reverts commit 4397786f9fd7f37cb6c2e4f00741a2343e9e4d57, reversing 
 changes made to 84d095558dcd61554c2a0a988977bb1e9eecb71d. 
- [84d095558dcd615](https://github.com/serenity-bdd/serenity-core/commit/84d095558dcd615) Refactoring of the report generation code to rectify #160
- [8fedb5437877646](https://github.com/serenity-bdd/serenity-core/commit/8fedb5437877646) Refactoring WebDriver integration to use the ThucydidesWebDriverSupport class
- [a1979bb7f938344](https://github.com/serenity-bdd/serenity-core/commit/a1979bb7f938344) 130_issue: removed emtpy lines
- [e8607afe6fb9998](https://github.com/serenity-bdd/serenity-core/commit/e8607afe6fb9998) 130_issue: fixed.  Added sample projects for testing serenity-gradle-plugin
- [322e572db71d9d6](https://github.com/serenity-bdd/serenity-core/commit/322e572db71d9d6) 130_issue: spelling error fix
- [28be7ba00561d2f](https://github.com/serenity-bdd/serenity-core/commit/28be7ba00561d2f) 130_issue: build.config updated for simple project for serenity-gradle_plugin
- [d5883dbac1b97c5](https://github.com/serenity-bdd/serenity-core/commit/d5883dbac1b97c5) 130_issue: updated simple-gradle-project for serenity-gradle-plugin
- [ee6807e845a9293](https://github.com/serenity-bdd/serenity-core/commit/ee6807e845a9293) 130_issue: updated simple-gradle-project for serenity-gradle-plugin
- [0c105044830f797](https://github.com/serenity-bdd/serenity-core/commit/0c105044830f797) 130_issue: added test and default project for gradle plugin
- [c66f0fe7113da4a](https://github.com/serenity-bdd/serenity-core/commit/c66f0fe7113da4a) Fixed an issue with the reporting of pending and skipped tests
- [d9eca6e184af361](https://github.com/serenity-bdd/serenity-core/commit/d9eca6e184af361) Fixed typo in the smoketests
- [c497bb6b231cdb7](https://github.com/serenity-bdd/serenity-core/commit/c497bb6b231cdb7) Updating dependencies for the smoketest project
- [a4dc59d0aa64b2d](https://github.com/serenity-bdd/serenity-core/commit/a4dc59d0aa64b2d) Fixed typo in the smoketests
- [ad774592904ec3e](https://github.com/serenity-bdd/serenity-core/commit/ad774592904ec3e) Made the instantiation of test steps more robust, mainly for use in the Journey pattern
### v1.1.17-rc.5
** Commits with examples **
- [d2f951a2b282659](https://github.com/serenity-bdd/serenity-core/commit/d2f951a2b282659) Added the serenity.error.on, serenity.fail.on and serenity.pending.on properties to the ThucydidesSystemProperty class.
- [3c397299c342b15](https://github.com/serenity-bdd/serenity-core/commit/3c397299c342b15) You can use the serenity.pending.on property to define exceptions that will cause a test to be marked as Pending.
- [032dbb615134963](https://github.com/serenity-bdd/serenity-core/commit/032dbb615134963) Added a general solution for defining or overriding how exceptions should be reported.
### v1.1.17-rc.4
** Commits with examples **
- [5d1b871b917e0c0](https://github.com/serenity-bdd/serenity-core/commit/5d1b871b917e0c0) Fixed an error in the freemarker templates.
- [271ffe108f5880f](https://github.com/serenity-bdd/serenity-core/commit/271ffe108f5880f) Added support for customising exception handling.
 You can now specify your own exceptions that will cause a failure by using the /serenity.fail.on/ property. You can also specify those that will cause an error using /serenity.error.on/. 
- [b2c29a9ed0f6e51](https://github.com/serenity-bdd/serenity-core/commit/b2c29a9ed0f6e51) Improved report icons
- [c58450593b567a1](https://github.com/serenity-bdd/serenity-core/commit/c58450593b567a1) Fixed some issues related to displaying manual tests
- [bafaead4743dd9d](https://github.com/serenity-bdd/serenity-core/commit/bafaead4743dd9d) Fixed some broken tests
- [2e959d4fef6356f](https://github.com/serenity-bdd/serenity-core/commit/2e959d4fef6356f) Fixed some broken tests
- [5fdc2be5bf86270](https://github.com/serenity-bdd/serenity-core/commit/5fdc2be5bf86270) Refactoring
- [157c616b2f9b519](https://github.com/serenity-bdd/serenity-core/commit/157c616b2f9b519) Trim Appium system properties
- [01a6e9d3a51cff8](https://github.com/serenity-bdd/serenity-core/commit/01a6e9d3a51cff8) Improved reporting
 Use FontAwesome for more readable test result icons. 
- [7de1dd5ba3fe508](https://github.com/serenity-bdd/serenity-core/commit/7de1dd5ba3fe508) Better error/failure distinction
 Exceptions such as ElementShouldBeInvisibleException are now reported as failures, not errors. 
- [2e0752d93e05f48](https://github.com/serenity-bdd/serenity-core/commit/2e0752d93e05f48) Added a more meaningful error message if a resource file cannot be copied.
### v1.1.17-rc.3
** Commits with examples **
- [b16d29a29509c8d](https://github.com/serenity-bdd/serenity-core/commit/b16d29a29509c8d) Refactoring
- [93f8e34a2747219](https://github.com/serenity-bdd/serenity-core/commit/93f8e34a2747219) Refactoring the html resource copying code.
- [4d6e9bc104b4a27](https://github.com/serenity-bdd/serenity-core/commit/4d6e9bc104b4a27) Refining support for multi-thread report generation to avoid contention on resource files
- [652c048ac985d1f](https://github.com/serenity-bdd/serenity-core/commit/652c048ac985d1f) Test that checks to see if the proxy driver class is returned when the the driver class is the provided driver
- [60ef04c4b8b46f4](https://github.com/serenity-bdd/serenity-core/commit/60ef04c4b8b46f4) Fix: Do not execute remaining steps after assumption failed
- [ad3af93eda7fa4a](https://github.com/serenity-bdd/serenity-core/commit/ad3af93eda7fa4a) Having ProvidedDriver implement JavascriptExecutor should not be the correct way to fix THUCYDIDES-253. The method that checks if the driver is javascript enabled looks at the driver class returned from WebDriverFacade and in the case, it will see that ProvidedDriver implements JavascriptExecutor but when it tries to execute javascript on the proxied driver that does not necessarily have to implement JavascriptExecutor, then it will throw a method not found exception. This proposed fix checks if the driverclass in the WebDriverFacade is a provided driver, if it is, then the correct driver class it should look at is contained in the proxied driver.
### v1.1.17-rc.2
** Commits with examples **
- [13edac4e25606fa](https://github.com/serenity-bdd/serenity-core/commit/13edac4e25606fa) Refactoring of a solution to avoid contention on resource JAR files.
- [fe753a880bb2dff](https://github.com/serenity-bdd/serenity-core/commit/fe753a880bb2dff) Fixed a test
- [496320a0c08f381](https://github.com/serenity-bdd/serenity-core/commit/496320a0c08f381) Ensure that HTML report resource files are only copied if they are not already present.
- [f195e492df7618f](https://github.com/serenity-bdd/serenity-core/commit/f195e492df7618f) Ignore warnings if we try to save a screenshot that already exists.
- [80dc1909929b502](https://github.com/serenity-bdd/serenity-core/commit/80dc1909929b502) Fixed a broken test
- [169b5e8fd721a0e](https://github.com/serenity-bdd/serenity-core/commit/169b5e8fd721a0e) Refactoring
- [93337a754212f36](https://github.com/serenity-bdd/serenity-core/commit/93337a754212f36) fix: correct unit test
- [8cff02bf05a93bf](https://github.com/serenity-bdd/serenity-core/commit/8cff02bf05a93bf) fix: stop further steps execution if test is suspended
- [e957030c91106c4](https://github.com/serenity-bdd/serenity-core/commit/e957030c91106c4) Refactored redundant tests
- [a83934edd78de54](https://github.com/serenity-bdd/serenity-core/commit/a83934edd78de54) Refactoring
- [0bcdbcfb461f8ce](https://github.com/serenity-bdd/serenity-core/commit/0bcdbcfb461f8ce) refactor: Corrects throwning of IOException, instead of Exception
- [ea10f238c429373](https://github.com/serenity-bdd/serenity-core/commit/ea10f238c429373) Refactoring
- [e0b51a437d355f9](https://github.com/serenity-bdd/serenity-core/commit/e0b51a437d355f9) fix loop when parameter is null in ddt tests
### v1.1.17-rc.1
** Commits with examples **
- [64af9acd1d8d9da](https://github.com/serenity-bdd/serenity-core/commit/64af9acd1d8d9da) The withTestDataFrom() method now accepts a list of strings as well as a CSV file.
- [d49c8b2f488adfe](https://github.com/serenity-bdd/serenity-core/commit/d49c8b2f488adfe) Added smoketest tags to illustrate using tags.
- [3dddb91bd54347d](https://github.com/serenity-bdd/serenity-core/commit/3dddb91bd54347d) Added a new sample data-driven test to the smoke tests
- [4f95fd346b7419e](https://github.com/serenity-bdd/serenity-core/commit/4f95fd346b7419e) Removed old screenshot processing logic
- [577dacf7f777583](https://github.com/serenity-bdd/serenity-core/commit/577dacf7f777583) chore: General test refactoring.
- [0b94e8daba308bc](https://github.com/serenity-bdd/serenity-core/commit/0b94e8daba308bc) Minor refactoring
 Added multi-thread testing for the screenshot pipeline, and removed misleading warnings that could happen when two threads try to save the same screenshot. 
- [e07f25002f7ec85](https://github.com/serenity-bdd/serenity-core/commit/e07f25002f7ec85) fix: Removed a potential issue where the screenshot target directory was not created correctly
- [ca53d5e75470fef](https://github.com/serenity-bdd/serenity-core/commit/ca53d5e75470fef) chore:test hardening
- [e1525d38bca5fc9](https://github.com/serenity-bdd/serenity-core/commit/e1525d38bca5fc9) Made the screenshot processing a bit more robust
- [01e59d1a7199b27](https://github.com/serenity-bdd/serenity-core/commit/01e59d1a7199b27) Fine-tuned the smoke test app
- [70db76ded080214](https://github.com/serenity-bdd/serenity-core/commit/70db76ded080214) Fine-tuned the smoke test app
- [929e14da0922d4b](https://github.com/serenity-bdd/serenity-core/commit/929e14da0922d4b) Added additional tests to the smoke test suite
- [2e315ec39b25021](https://github.com/serenity-bdd/serenity-core/commit/2e315ec39b25021) chore:Refactoring and tidying up the code
- [2341b7409624050](https://github.com/serenity-bdd/serenity-core/commit/2341b7409624050) [JDK7 compatibility] Corrections to maintain JDK7 compatibility
 Replace usage of java Optional with Guava optional 
- [37aa19d2ddef10c](https://github.com/serenity-bdd/serenity-core/commit/37aa19d2ddef10c) Added smoke tests
- [1b84d2e7d7b33aa](https://github.com/serenity-bdd/serenity-core/commit/1b84d2e7d7b33aa) fix: Handle empty screenshots without crashing.
- [825328a5cd76f7d](https://github.com/serenity-bdd/serenity-core/commit/825328a5cd76f7d) Added the Todo app smoke tests
- [f20daf748843c6b](https://github.com/serenity-bdd/serenity-core/commit/f20daf748843c6b) Refactored the screenshot processing logic
### v1.1.16
** Commits with examples **
- [632a91a024abd3b](https://github.com/serenity-bdd/serenity-core/commit/632a91a024abd3b) Refactoring
- [975f25e90c30c25](https://github.com/serenity-bdd/serenity-core/commit/975f25e90c30c25) Updated dependencies
- [3fc89becc4c606b](https://github.com/serenity-bdd/serenity-core/commit/3fc89becc4c606b) Removed unnused imports
- [395632770ed8fc1](https://github.com/serenity-bdd/serenity-core/commit/395632770ed8fc1) Just trigger rebuild
### v1.1.15
** Commits with examples **
- [020fd6fa6e101f6](https://github.com/serenity-bdd/serenity-core/commit/020fd6fa6e101f6) build:refactoring test phase
- [0068f01d15df7dc](https://github.com/serenity-bdd/serenity-core/commit/0068f01d15df7dc) Deprecated old screenshot processor
- [92fc1c67d24fb6e](https://github.com/serenity-bdd/serenity-core/commit/92fc1c67d24fb6e) Deprecated old screenshot processor
- [f4670d119a6c8ec](https://github.com/serenity-bdd/serenity-core/commit/f4670d119a6c8ec) Deprecated old screenshot processor
- [84e1e5f25cd5bac](https://github.com/serenity-bdd/serenity-core/commit/84e1e5f25cd5bac) Deprecated old screenshot processor
- [ad43f431f450dac](https://github.com/serenity-bdd/serenity-core/commit/ad43f431f450dac) refactor:fine-tuning build job
- [60fa70b080f1200](https://github.com/serenity-bdd/serenity-core/commit/60fa70b080f1200) refactor:Better error handling for screenshots
- [29b129c8ef92e3c](https://github.com/serenity-bdd/serenity-core/commit/29b129c8ef92e3c) refactor:Better error handling for screenshots
- [9bd7368cbb05b3b](https://github.com/serenity-bdd/serenity-core/commit/9bd7368cbb05b3b) refactor:Better error handling for screenshots
- [4bfc541c331a6e9](https://github.com/serenity-bdd/serenity-core/commit/4bfc541c331a6e9) refactor:Better error handling for screenshots
- [f5c5fc76afcc3b0](https://github.com/serenity-bdd/serenity-core/commit/f5c5fc76afcc3b0) refactor:Better error handling for screenshots
- [0bfbd9578a80bf1](https://github.com/serenity-bdd/serenity-core/commit/0bfbd9578a80bf1) refactor:Removed old screenshot logic
- [8d77bc49dfa524b](https://github.com/serenity-bdd/serenity-core/commit/8d77bc49dfa524b) fix: Fixed a memory leak.
- [5e392c973fb53eb](https://github.com/serenity-bdd/serenity-core/commit/5e392c973fb53eb) refactor:Removed old screenshot logic
- [1599557cf37ab9d](https://github.com/serenity-bdd/serenity-core/commit/1599557cf37ab9d) Added new implementation of the screenshot logic
- [252524c9056b047](https://github.com/serenity-bdd/serenity-core/commit/252524c9056b047) Inital version of a new implementation of the screenshot logic.
- [91ffac148057562](https://github.com/serenity-bdd/serenity-core/commit/91ffac148057562) Added support for blurring.
- [f84df26505988ea](https://github.com/serenity-bdd/serenity-core/commit/f84df26505988ea) Inital version of a new implementation of the screenshot logic.
- [80913b94b709b8b](https://github.com/serenity-bdd/serenity-core/commit/80913b94b709b8b) chore:Added the chromedriver binary for the Snap-CI builds
- [461c7843410b9f4](https://github.com/serenity-bdd/serenity-core/commit/461c7843410b9f4) fix: Checks if driver is not null (before calling close() )
- [540ce87d44b93cb](https://github.com/serenity-bdd/serenity-core/commit/540ce87d44b93cb) fix: Adds JAVA_HOME to the environment (map) in case the key / value is
 not available from the System.getenv() 
- [cf774f8d24741dc](https://github.com/serenity-bdd/serenity-core/commit/cf774f8d24741dc) refactor: Added better error handling for the actors.
- [9e7e55695924f47](https://github.com/serenity-bdd/serenity-core/commit/9e7e55695924f47) fix: Checks if the driver != null, before calling close() and quit(),
- [7578ed2ff16cf34](https://github.com/serenity-bdd/serenity-core/commit/7578ed2ff16cf34) fix: Checks if the driver != null, before calling close() and quit(),
- [666e9dcfd8d8df3](https://github.com/serenity-bdd/serenity-core/commit/666e9dcfd8d8df3) refactor: Removes maven-easyb-plugin, is not used, or correct me if I&#39;m
 wrong. 
- [1381ebdaa955146](https://github.com/serenity-bdd/serenity-core/commit/1381ebdaa955146) refactor: Removes warning that log4j was not initialized
 Updates thucydides-core with exclusion of log4j 
 Adds dependency log4j-over-slf4j 
- [6200d4effd5470a](https://github.com/serenity-bdd/serenity-core/commit/6200d4effd5470a) fix: Updates default URL to &#39;http://www.google.com/ncr&#39; this prevents
 redirects from &#39;google.com&#39; to country specific google search pages. 
- [94cf1d57fad63a1](https://github.com/serenity-bdd/serenity-core/commit/94cf1d57fad63a1) fix: Corrects auto redirect to secure connection (https instead of http)
- [6148fe2833f5e7f](https://github.com/serenity-bdd/serenity-core/commit/6148fe2833f5e7f) docs: Adds description how to correct add chrome-web-driver
- [365388539e0dfc3](https://github.com/serenity-bdd/serenity-core/commit/365388539e0dfc3) docs: Adds description about the Serenity Demo
- [5556ddae9469a43](https://github.com/serenity-bdd/serenity-core/commit/5556ddae9469a43) chore: Adds profiles &#39;firefox&#39; and &#39;chrome&#39;, for easier running the
 tests with different browsers. 
- [a860b0bb5f3b58f](https://github.com/serenity-bdd/serenity-core/commit/a860b0bb5f3b58f) fix: Corrects issue with auto redirect to secure connection (https
 instead of http) 
- [7d21048e9a2b3b0](https://github.com/serenity-bdd/serenity-core/commit/7d21048e9a2b3b0) fix: Corrects issue auto forwarding from google.com to google.xxx the
 country specific search page. 
- [476a18322150cbb](https://github.com/serenity-bdd/serenity-core/commit/476a18322150cbb) fix: Updates dependencies to latest stable release 0.8
 thucydides-junit 0.8.31 (was 0.8.1-SNAPSHTOT) 
 thucydides-core  0.8.31 (was 0.8.1-SNAPSHTOT) 
 Adds dependency 
 slf4j-simple  1.6.4 
- [7974322366574a3](https://github.com/serenity-bdd/serenity-core/commit/7974322366574a3) fix: Brings package name in class inline with the package directory
 structure 
- [7b58b52e3c13baa](https://github.com/serenity-bdd/serenity-core/commit/7b58b52e3c13baa) Renames package &#39;net.serenity_bdd.*&#39; into &#39;net.serenitybdd.*&#39;, to bring
 them inline with the rest 
- [33fac2e859d6bc7](https://github.com/serenity-bdd/serenity-core/commit/33fac2e859d6bc7) Removes unused imports
- [618a81345bdd93c](https://github.com/serenity-bdd/serenity-core/commit/618a81345bdd93c) Removes unused variable registeredWebdriverManagers
- [b57fce26d9baea8](https://github.com/serenity-bdd/serenity-core/commit/b57fce26d9baea8) Removes unused import
- [4cf4c1123a50402](https://github.com/serenity-bdd/serenity-core/commit/4cf4c1123a50402) Removes generics warning
- [8cfa26db66a93f2](https://github.com/serenity-bdd/serenity-core/commit/8cfa26db66a93f2) Removes no longer needed @SuppressWarnings
- [d370f8441d4d146](https://github.com/serenity-bdd/serenity-core/commit/d370f8441d4d146) Removes generics warnings
- [4318dc2a8180f75](https://github.com/serenity-bdd/serenity-core/commit/4318dc2a8180f75) Removes warning &#39;Use static field LoggingLevel.VERBOSE&#39;
- [99c05b534ed9d49](https://github.com/serenity-bdd/serenity-core/commit/99c05b534ed9d49) Removes @SuppressWarnings, no longer needed
- [910356643cb2257](https://github.com/serenity-bdd/serenity-core/commit/910356643cb2257) Removes unsued variable
- [52a42c40edd6b9b](https://github.com/serenity-bdd/serenity-core/commit/52a42c40edd6b9b) Fixes generics issue (no longer warning)
- [bf415be9811359f](https://github.com/serenity-bdd/serenity-core/commit/bf415be9811359f) Removes unused imports
- [f38011c61aa04c6](https://github.com/serenity-bdd/serenity-core/commit/f38011c61aa04c6) Corrects javadoc description
- [dc6c68e81a9031e](https://github.com/serenity-bdd/serenity-core/commit/dc6c68e81a9031e) Simplified a unit test
- [6c0391deaec315d](https://github.com/serenity-bdd/serenity-core/commit/6c0391deaec315d) Simplified a unit test
- [20f7f3075e538f3](https://github.com/serenity-bdd/serenity-core/commit/20f7f3075e538f3) Fixed an error in the reporting in the Hit interaction
- [917ff5d67fbce78](https://github.com/serenity-bdd/serenity-core/commit/917ff5d67fbce78) Fixed project build on Windows
### v1.1.14
** Commits with examples **
- [c7658dfd48b8fdd](https://github.com/serenity-bdd/serenity-core/commit/c7658dfd48b8fdd) Test refactoring
- [5d16f7a17ee6056](https://github.com/serenity-bdd/serenity-core/commit/5d16f7a17ee6056) Removed the redundant &#39;Stabie&#39; column in the reports
- [0f4803e013ed331](https://github.com/serenity-bdd/serenity-core/commit/0f4803e013ed331) Better error reporting for actors in the Journey module.
- [05a1789883ec4e4](https://github.com/serenity-bdd/serenity-core/commit/05a1789883ec4e4) Improved logging messages
- [9af3f06f1329590](https://github.com/serenity-bdd/serenity-core/commit/9af3f06f1329590) Better support for BrowserStack capability options
- [7e181098f94ff32](https://github.com/serenity-bdd/serenity-core/commit/7e181098f94ff32) Added &#39;feature.file.encoding&#39; system property to specify an encoding of Cucumber files
### v1.1.13
** Commits with examples **
- [d131e1535be9ee2](https://github.com/serenity-bdd/serenity-core/commit/d131e1535be9ee2) Fixed an issue with taking screenshots when using multiple browsers
- [48305b4dfdf4d31](https://github.com/serenity-bdd/serenity-core/commit/48305b4dfdf4d31) Fixed an issue with the moveTo() PageObject method
- [1c3eb5e7fa91c9a](https://github.com/serenity-bdd/serenity-core/commit/1c3eb5e7fa91c9a) Fixed an issue that caused tests with multiple actors to report steps out of order.
### v1.1.12
** Commits with examples **
- [89461ce6f7eeb53](https://github.com/serenity-bdd/serenity-core/commit/89461ce6f7eeb53) Additional requirements testing
- [b843013bf18cb0e](https://github.com/serenity-bdd/serenity-core/commit/b843013bf18cb0e) Updated selenium core
- [ef0a39f8ad5fd3e](https://github.com/serenity-bdd/serenity-core/commit/ef0a39f8ad5fd3e) Updated selenium to 2.47.1
### v1.1.11
** Commits with examples **
- [65eada22ba2665f](https://github.com/serenity-bdd/serenity-core/commit/65eada22ba2665f) Better support for multiple browser management.
- [5f69b1bc6d82798](https://github.com/serenity-bdd/serenity-core/commit/5f69b1bc6d82798) Refactored screenshot-related logging to DEBUG
- [714f2a9025f8efe](https://github.com/serenity-bdd/serenity-core/commit/714f2a9025f8efe) Improved the step message when an actor enteres a value into a field.
### v1.1.10
** Commits with examples **
- [3721d0ab6bd6369](https://github.com/serenity-bdd/serenity-core/commit/3721d0ab6bd6369) Improved log reporting for the Journey pattern.
- [969c74b4f4838cd](https://github.com/serenity-bdd/serenity-core/commit/969c74b4f4838cd) Improved reporting in the console logging.
- [66cffe7b361595b](https://github.com/serenity-bdd/serenity-core/commit/66cffe7b361595b) fix: prevent null pointers when generating reports
### v1.1.9
** Commits with examples **
- [9051d518de25ee8](https://github.com/serenity-bdd/serenity-core/commit/9051d518de25ee8) Updated dependencies
### v1.1.8
** Commits with examples **
- [9bd70c2429c11b7](https://github.com/serenity-bdd/serenity-core/commit/9bd70c2429c11b7) Changed dependencies back to mockito 1.9.5 to avoid dependency conflict issues
- [45f1eae8491c8d9](https://github.com/serenity-bdd/serenity-core/commit/45f1eae8491c8d9) Test refactoring
- [32f488557eea780](https://github.com/serenity-bdd/serenity-core/commit/32f488557eea780) Fixed #115
 Only record REST responses for non-binary response types. 
- [de2d4287aab991f](https://github.com/serenity-bdd/serenity-core/commit/de2d4287aab991f) Attempt to fix #122
- [1bdbc53a34dba3b](https://github.com/serenity-bdd/serenity-core/commit/1bdbc53a34dba3b) see https://github.com/serenity-bdd/serenity-core/issues/37
- [cbfb1788cd8e35a](https://github.com/serenity-bdd/serenity-core/commit/cbfb1788cd8e35a) Fixing Java warnings - Redundant cast
 GoogleSearchSteps.java:27: warning: [cast] redundant cast to GoogleHomePage 
 GoogleHomePage page = (GoogleHomePage) getPages().currentPageAt(GoogleHomePage.class); 
 GoogleSearchSteps.java:33: warning: [cast] redundant cast to GoogleResultsPage 
 GoogleResultsPage page = (GoogleResultsPage) getPages().currentPageAt(GoogleResultsPage.class); 
- [c6ed01d846f4646](https://github.com/serenity-bdd/serenity-core/commit/c6ed01d846f4646) Added support for multiple browsers in the same test using the Journey pattern
 For example: 
 @Managed(driver=&quot;chrome&quot;) 
 WebDriver firstBrowser; 
 @Managed(driver=&quot;firefox&quot;) 
 WebDriver anotherBrowser; 
 @Test 
 public void danaCanUpdateHerProfile() { 
 Actor dana = new Actor(&quot;Dana&quot;); 
 dana.can(BrowseTheWeb.with(firstBrowser)); 
 givenThat(dana).has(openedTheApplication); 
 when(dana).attemptsTo(viewHerProfile); 
 and(dana).attemptsTo(UpdateHerProfile.withName(&quot;Dana&quot;).andCountryOfResidence(&quot;France&quot;)); 
 then(dana).should(seeThat(TheProfile.name(), equalTo(&quot;Dana&quot;))); 
 and(dana).should(seeThat(TheProfile.country(), equalTo(&quot;France&quot;))); 
- [a8ae2e5f4ac22d1](https://github.com/serenity-bdd/serenity-core/commit/a8ae2e5f4ac22d1) Debug log: Adding exception to output
 Sample output: 
 11:29:07.868 [Test worker] DEBUG n.s.j.r.RetryFilteringRunNotifier - Test failed: com.skagenfondene.test.stories.InactiveUser: java.lang.NullPointerException--&gt;null 
 net.sf.cglib.core.CodeGenerationException: java.lang.NullPointerException--&gt;null 
 at net.sf.cglib.core.ReflectUtils.newInstance(ReflectUtils.java:235) ~[cglib-3.1.jar:na] 
 at net.sf.cglib.core.ReflectUtils.newInstance(ReflectUtils.java:220) ~[cglib-3.1.jar:na] 
 at net.sf.cglib.proxy.Enhancer.createUsingReflection(Enhancer.java:639) ~[cglib-3.1.jar:na] 
 at net.sf.cglib.proxy.Enhancer.firstInstance(Enhancer.java:538) ~[cglib-3.1.jar:na] 
 at net.sf.cglib.core.AbstractClassGenerator.create(AbstractClassGenerator.java:225) ~[cglib-3.1.jar:na] 
 at net.sf.cglib.proxy.Enhancer.createHelper(Enhancer.java:377) ~[cglib-3.1.jar:na] 
 at net.sf.cglib.proxy.Enhancer.create(Enhancer.java:304) ~[cglib-3.1.jar:na] 
 at net.thucydides.core.steps.StepFactory.webEnabledStepLibrary(StepFactory.java:167) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepFactory.createProxyStepLibrary(StepFactory.java:157) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepFactory.instantiateNewStepLibraryFor(StepFactory.java:111) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepFactory.instantiateNewStepLibraryFor(StepFactory.java:103) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepFactory.getNewStepLibraryFor(StepFactory.java:75) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepFactory.getStepLibraryFor(StepFactory.java:70) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepAnnotations.instantiateAnyUnitiaializedSteps(StepAnnotations.java:52) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepAnnotations.instanciateScenarioStepFields(StepAnnotations.java:41) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.thucydides.core.steps.StepAnnotations.injectScenarioStepsInto(StepAnnotations.java:23) ~[serenity-core-1.1.5.jar:1.1.5] 
 at net.serenitybdd.junit.runners.SerenityRunner.injectScenarioStepsInto(SerenityRunner.java:590) [serenity-junit-1.1.5.jar:na] 
 at net.serenitybdd.junit.runners.SerenityRunner.methodInvoker(SerenityRunner.java:552) [serenity-junit-1.1.5.jar:na] 
 at org.junit.runners.BlockJUnit4ClassRunner.methodBlock(BlockJUnit4ClassRunner.java:251) ~[junit-4.11.jar:na] 
 at org.junit.runners.BlockJUnit4ClassRunner.runChild(BlockJUnit4ClassRunner.java:70) ~[junit-4.11.jar:na] 
 at net.serenitybdd.junit.runners.SerenityRunner.runChild(SerenityRunner.java:440) [serenity-junit-1.1.5.jar:na] 
 at net.serenitybdd.junit.runners.SerenityRunner.runChild(SerenityRunner.java:60) [serenity-junit-1.1.5.jar:na] 
 at org.junit.runners.ParentRunner$3.run(ParentRunner.java:238) ~[junit-4.11.jar:na] 
 at org.junit.runners.ParentRunner$1.schedule(ParentRunner.java:63) ~[junit-4.11.jar:na] 
 at org.junit.runners.ParentRunner.runChildren(ParentRunner.java:236) ~[junit-4.11.jar:na] 
 at org.junit.runners.ParentRunner.access$000(ParentRunner.java:53) ~[junit-4.11.jar:na] 
 at org.junit.runners.ParentRunner$2.evaluate(ParentRunner.java:229) ~[junit-4.11.jar:na] 
 at org.junit.runners.ParentRunner.run(ParentRunner.java:309) ~[junit-4.11.jar:na] 
 at net.serenitybdd.junit.runners.SerenityRunner.run(SerenityRunner.java:249) [serenity-junit-1.1.5.jar:na] 
 at org.gradle.api.internal.tasks.testing.junit.JUnitTestClassExecuter.runTestClass(JUnitTestClassExecuter.java:86) [gradle-plugins-2.2.1.jar:2.2.1] 
 at org.gradle.api.internal.tasks.testing.junit.JUnitTestClassExecuter.execute(JUnitTestClassExecuter.java:49) [gradle-plugins-2.2.1.jar:2.2.1] 
 at org.gradle.api.internal.tasks.testing.junit.JUnitTestClassProcessor.processTestClass(JUnitTestClassProcessor.java:69) [gradle-plugins-2.2.1.jar:2.2.1] 
 at org.gradle.api.internal.tasks.testing.SuiteTestClassProcessor.processTestClass(SuiteTestClassProcessor.java:48) [gradle-plugins-2.2.1.jar:2.2.1] 
 at sun.reflect.NativeMethodAccessorImpl.invoke0(Native Method) ~[na:1.8.0_05] 
 at sun.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62) ~[na:1.8.0_05] 
 at sun.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43) ~[na:1.8.0_05] 
 at java.lang.reflect.Method.invoke(Method.java:483) ~[na:1.8.0_05] 
 at org.gradle.messaging.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:35) [gradle-messaging-2.2.1.jar:2.2.1] 
 at org.gradle.messaging.dispatch.ReflectionDispatch.dispatch(ReflectionDispatch.java:24) [gradle-messaging-2.2.1.jar:2.2.1] 
 at org.gradle.messaging.dispatch.ContextClassLoaderDispatch.dispatch(ContextClassLoaderDispatch.java:32) [gradle-messaging-2.2.1.jar:2.2.1] 
 at org.gradle.messaging.dispatch.ProxyDispatchAdapter$DispatchingInvocationHandler.invoke(ProxyDispatchAdapter.java:93) [gradle-messaging-2.2.1.jar:2.2.1] 
 at com.sun.proxy.$Proxy2.processTestClass(Unknown Source) [na:na] 
- [9eeabc7e93e6b9b](https://github.com/serenity-bdd/serenity-core/commit/9eeabc7e93e6b9b) Improving logging in ReportService
- [2f1bf50b655c68a](https://github.com/serenity-bdd/serenity-core/commit/2f1bf50b655c68a) feat: the phantomjs ssl-property can now be set using the PHANTOMJS_SSL_PROPERTY environment variable, like the PHANTOMJS_BINARY_PATH. Possible options are &#39;sslv2&#39;, &#39;sslv3&#39;, &#39;tlsv1&#39; and &#39;any&#39;.
### v1.1.7
** Commits with examples **
- [75415857c76fa70](https://github.com/serenity-bdd/serenity-core/commit/75415857c76fa70) Better integration of Actors and Question objects
 Actors can now ask questions directly, e.g. 
 --- 
 Integer totalCost = dana.asksFor(theTotalCost()); 
 --- 
 They can also remember the answers to questions for future use: 
 --- 
 dana.remember(&quot;Total Cost&quot;, theTotalCost()); 
 assertThat(dana.recall(&quot;Total Cost&quot;)).isEqualTo(14); 
 --- 
### v1.1.6
** Commits with examples **
- [f77a999a3f1fe3c](https://github.com/serenity-bdd/serenity-core/commit/f77a999a3f1fe3c) Refactoring and better console reporting.
- [a2089724582c419](https://github.com/serenity-bdd/serenity-core/commit/a2089724582c419) Ensure that Consequence steps are not evaluated after a previous step has failed.
 This avoids misleading error messages. 
- [4404ea3c9f3c91b](https://github.com/serenity-bdd/serenity-core/commit/4404ea3c9f3c91b) Refactored the journey demo test
 To better illustrate tasks/interaction layers. 
- [f7dc3d73a581aa9](https://github.com/serenity-bdd/serenity-core/commit/f7dc3d73a581aa9) Added support for dropdowns in the interaction-level bundled Performables.
- [d3d2e38936d3979](https://github.com/serenity-bdd/serenity-core/commit/d3d2e38936d3979) Removed unnecessary warning messages
- [743ec7b5c289e57](https://github.com/serenity-bdd/serenity-core/commit/743ec7b5c289e57) Revolving dependency conflicts with hamcrest 1.1
- [3006a4ea233ddc9](https://github.com/serenity-bdd/serenity-core/commit/3006a4ea233ddc9) fix: Improved error reporting for provided drivers
 DriverSources may implement some non-trivial logic, so it is very handy 
 for debugging to include in stack trace exception occurred while tried to 
 initialize new webdriver. Especially in multi-node test environment 
 configurations. 
- [63458448580c2b0](https://github.com/serenity-bdd/serenity-core/commit/63458448580c2b0) Removed redundant code that was causing errors in the reports.
 If there were more than one given clause in a journey-style test, the initial givens where incorrectly nested. 
### v1.1.5
** Commits with examples **
- [b7a8e7190bf7486](https://github.com/serenity-bdd/serenity-core/commit/b7a8e7190bf7486) Avoid unnecessary error messages with Java 8 lambdas.
- [d7af4ed258615c6](https://github.com/serenity-bdd/serenity-core/commit/d7af4ed258615c6) Fixed class conflict issue.
- [3afdafb4c61939c](https://github.com/serenity-bdd/serenity-core/commit/3afdafb4c61939c) Improved reporting of questions
- [08c6aab6d2797bc](https://github.com/serenity-bdd/serenity-core/commit/08c6aab6d2797bc) Renamed &#39;serenity-ability-to-browse-the-web&#39; to &#39;browse-the-web&#39;
- [ed62f9307eb62e7](https://github.com/serenity-bdd/serenity-core/commit/ed62f9307eb62e7) Added the &quot;ability-to-browse-the-web&quot; module to the journey module.
- [8bec974f768f3c8](https://github.com/serenity-bdd/serenity-core/commit/8bec974f768f3c8) Fix inject Pages in super class
- [b06d96153f9ed78](https://github.com/serenity-bdd/serenity-core/commit/b06d96153f9ed78) Fix #109
- [cfb3bd63f86fd3f](https://github.com/serenity-bdd/serenity-core/commit/cfb3bd63f86fd3f) Check for existence of the angular object.
- [d64e692974cc952](https://github.com/serenity-bdd/serenity-core/commit/d64e692974cc952) Refactoring build
### v1.1.4
** Commits with examples **
- [d29c52eeab26550](https://github.com/serenity-bdd/serenity-core/commit/d29c52eeab26550) Minor refactoring
- [65da5169c348795](https://github.com/serenity-bdd/serenity-core/commit/65da5169c348795) Added the Question as a concept.
- [7848a32e8265882](https://github.com/serenity-bdd/serenity-core/commit/7848a32e8265882) Test refactoring
- [7ae80bfa70188b9](https://github.com/serenity-bdd/serenity-core/commit/7ae80bfa70188b9) Test refactoring
- [9722c9025f24bef](https://github.com/serenity-bdd/serenity-core/commit/9722c9025f24bef) You can now include assertions in the tests
 You can now include assertions in the tests and reports using the Consequence class. 
- [eeb1f7353ea5466](https://github.com/serenity-bdd/serenity-core/commit/eeb1f7353ea5466) Works for nested failing tasks
- [5ee8c7e4cd29642](https://github.com/serenity-bdd/serenity-core/commit/5ee8c7e4cd29642) Report task steps correctly when an error occurs in a task step
- [9e49f8c1d500cc2](https://github.com/serenity-bdd/serenity-core/commit/9e49f8c1d500cc2) Got successful and failing journey scenarios working, as long as the failing assertion is in the performAs method. Currently, if one of the chained methods fails, the following steps are not executed and the results are unpredictable
- [7f8f10c771f3dba](https://github.com/serenity-bdd/serenity-core/commit/7f8f10c771f3dba) Fix issue #106
- [95aa4af410f5c73](https://github.com/serenity-bdd/serenity-core/commit/95aa4af410f5c73) You can now use #this or #self in a @Step description.
- [968c4030467adf7](https://github.com/serenity-bdd/serenity-core/commit/968c4030467adf7) Better treatment of invalid or undefined fields in step definitions.
- [7755f2efdada037](https://github.com/serenity-bdd/serenity-core/commit/7755f2efdada037) Simplified variable injection into step descriptions.
 You can now inject any member variable in the step class by name into step descriptions 
 You can now use member variables of a step library in the @Step annotation to augment the step description. Just refer to the variable using the name of the variable prefixed by a &quot;#&quot;, as shown in this example: 
 ---- 
 private final String siteName = &quot;Etsy&quot;; 
 @Step(&quot;Search for a shop called {0} on the #siteName website&quot;) 
 public void searches_for_shop_called(String shopName) { 
 homePage.searchForShopCalled(shopName); 
 } 
 ---- 
- [f353c363ae54e52](https://github.com/serenity-bdd/serenity-core/commit/f353c363ae54e52) Refactoring
- [cd553eb90d77547](https://github.com/serenity-bdd/serenity-core/commit/cd553eb90d77547) Improve readability of &quot;View stack trace&quot; dialog (#103)
- [9b7c6025d8fef90](https://github.com/serenity-bdd/serenity-core/commit/9b7c6025d8fef90) Inject step variables by name into step descriptions
 You can now use member variables of a step library in the @Step annotation to augment the step description. Just refer to the variable using the name of the variable prefixed by a &quot;#&quot;, as shown in this example: 
 ---- 
 @Reported 
 private final String siteName = &quot;Etsy&quot;; 
 @Step(&quot;Search for a shop called {0} on the #siteName website&quot;) 
 public void searches_for_shop_called(String shopName) { 
 homePage.searchForShopCalled(shopName); 
 } 
 ---- 
- [c0b0fffc15caa85](https://github.com/serenity-bdd/serenity-core/commit/c0b0fffc15caa85) Added support for TypeSafeConfig
 You can now provide a TypeSafeConfig configuration file (https://github.com/typesafehub/config) instead of a serenity.properties file. The file can be called &#39;serenity.conf&#39; or any of the other Type Safe Config configuration files names. 
 The configuration file can contain both Serenity variables and other arbitrary variables, which will be available in the EnvironmentVariables field. For example, a simple configuration file might look like this. 
 ---- 
 serenity { 
 logging = DEBUG 
 } 
 environment { 
 uat = uat-server 
 } 
 ---- 
- [e50e5578683e887](https://github.com/serenity-bdd/serenity-core/commit/e50e5578683e887) Refactored a unit test for more clarity
### v1.1.3
** Commits with examples **
- [71f56847e32e7a9](https://github.com/serenity-bdd/serenity-core/commit/71f56847e32e7a9) Fixed an issue causing the drivers to be closed incorrectly during parallel tests
### v1.1.2
** Commits with examples **
- [6aae0d4539b3142](https://github.com/serenity-bdd/serenity-core/commit/6aae0d4539b3142) Added the &#39;uniqueInstance&#39; attribute to the @Steps annotation to support multiple instances of the same step library in the same class
- [c4033eaa90b53ff](https://github.com/serenity-bdd/serenity-core/commit/c4033eaa90b53ff) Fixed colors in some of the reports causing text to be light grey on white
### v1.1.1
** Commits with examples **
- [4c85801565208d6](https://github.com/serenity-bdd/serenity-core/commit/4c85801565208d6) Updated unit tests for manual tests
- [b8190993a962b85](https://github.com/serenity-bdd/serenity-core/commit/b8190993a962b85) Added support for manual annotated tests
- [312a8ec943d0094](https://github.com/serenity-bdd/serenity-core/commit/312a8ec943d0094) Fixed an issue that caused broken links in JUnit and Cucumber requirements reports
- [30c89b8286c0378](https://github.com/serenity-bdd/serenity-core/commit/30c89b8286c0378) Adding support for manual tests
### v1.1.0
** Commits with examples **
- [26c716c69e9a2ee](https://github.com/serenity-bdd/serenity-core/commit/26c716c69e9a2ee) Simplified some redundant tests
- [d4222f315f744b6](https://github.com/serenity-bdd/serenity-core/commit/d4222f315f744b6) JSON requirements files are now stored in a dedicated &#39;requirements&#39; directory.
- [3fd16d7b62a7770](https://github.com/serenity-bdd/serenity-core/commit/3fd16d7b62a7770) Minor refactoring
- [fc33695ff16e8fb](https://github.com/serenity-bdd/serenity-core/commit/fc33695ff16e8fb) Refactoring tests
- [8b837b624eae592](https://github.com/serenity-bdd/serenity-core/commit/8b837b624eae592) Upgraded to cucumber-jvm 1.2.4
- [31b954c14c634fa](https://github.com/serenity-bdd/serenity-core/commit/31b954c14c634fa) Upgraded to cucumber-jvm 1.2.4
- [1d3b1039c1e1c02](https://github.com/serenity-bdd/serenity-core/commit/1d3b1039c1e1c02) Requirements reporting now support mixing JBehave and JUnit tests.
- [869b7276a4defa3](https://github.com/serenity-bdd/serenity-core/commit/869b7276a4defa3) Fixed an issue with JBehave where the browser was not closing after tests.
- [5d78861f5501df9](https://github.com/serenity-bdd/serenity-core/commit/5d78861f5501df9) More consistent breadcrumbs
- [8797dae10c1fae3](https://github.com/serenity-bdd/serenity-core/commit/8797dae10c1fae3) Minor bug fixes
- [9c94af955b05e0f](https://github.com/serenity-bdd/serenity-core/commit/9c94af955b05e0f) Added the &#39;deep.step.execution.after.failures&#39; option
 This option (set to false by default), lets you control the execution depth of the @Step methods after a step has failed. If set to true, it will run nested @Step methods as well as top-level ones. 
- [7e82d4f3b315f58](https://github.com/serenity-bdd/serenity-core/commit/7e82d4f3b315f58) Include the name of the exception in error messages
- [6d3847c93b9c330](https://github.com/serenity-bdd/serenity-core/commit/6d3847c93b9c330) Refactored JSON file loading for better error reporting
- [8e6e206ac33e52d](https://github.com/serenity-bdd/serenity-core/commit/8e6e206ac33e52d) Added more robust support for running REST tests in DryRun mode.
- [e32a2a0099755f3](https://github.com/serenity-bdd/serenity-core/commit/e32a2a0099755f3) Improved reporting for tag-related reports
- [f5fbb68ad3d7b54](https://github.com/serenity-bdd/serenity-core/commit/f5fbb68ad3d7b54) Requirements breadcrumbs for JBehave
- [1764651aff9b8a7](https://github.com/serenity-bdd/serenity-core/commit/1764651aff9b8a7) Fixed a timeout issue.
 Fixed a timeout issue related to using withTimeoutOf(...).waitForElementToDisappear() 
- [bcc83dd04ebc0a8](https://github.com/serenity-bdd/serenity-core/commit/bcc83dd04ebc0a8) Added a utility method to wait for an AngularJS page to load properly.
- [4b5298def11a998](https://github.com/serenity-bdd/serenity-core/commit/4b5298def11a998) Removed thread leak issue
- [7a57c62bcb1dff0](https://github.com/serenity-bdd/serenity-core/commit/7a57c62bcb1dff0) Added basic support for the &#39;dry-run&#39; option.
 Rest calls will now be skipped if you activtate &#39;dry-run&#39; mode (e.g. by setting the &#39;serenity.dry.run&#39; system property to true). 
- [b3c78559ba2cc36](https://github.com/serenity-bdd/serenity-core/commit/b3c78559ba2cc36) refactoring requirements processing - wip
- [c2e028ca2847e22](https://github.com/serenity-bdd/serenity-core/commit/c2e028ca2847e22) Update BrowserStackRemoteDriverCapabilities.java
- [e64d7a75f03e723](https://github.com/serenity-bdd/serenity-core/commit/e64d7a75f03e723) Improved error reporting.
- [c14bdf6c5034ed7](https://github.com/serenity-bdd/serenity-core/commit/c14bdf6c5034ed7) Added support for XML REST messages
- [8ed69d8a271bc4a](https://github.com/serenity-bdd/serenity-core/commit/8ed69d8a271bc4a) Display the overall time taken for the tests
- [06ccc69767b8287](https://github.com/serenity-bdd/serenity-core/commit/06ccc69767b8287) Moved the screenshot caption to the top of the screenshots to make it easier to see
- [a66cef5da958b5f](https://github.com/serenity-bdd/serenity-core/commit/a66cef5da958b5f) Updated appium version
### v1.0.64
** Commits with examples **
- [21b96f814fd53d6](https://github.com/serenity-bdd/serenity-core/commit/21b96f814fd53d6) fix: Improved error messages for remote drivers
 Better error message reporting if a remote driver is incorrectly configured, and some minor refactoring. 
- [404d3bf2f6bdec1](https://github.com/serenity-bdd/serenity-core/commit/404d3bf2f6bdec1) chore:reinstated Bintray plugin
### v1.0.62
** Commits with examples **
- [85c600129e4c94b](https://github.com/serenity-bdd/serenity-core/commit/85c600129e4c94b) chore:Updating release plugins
- [5a907598c5f0f06](https://github.com/serenity-bdd/serenity-core/commit/5a907598c5f0f06) chore: Removed unnecessary wrapper directories
### v1.0.61
** Commits with examples **
- [0fbada91e9c3ccf](https://github.com/serenity-bdd/serenity-core/commit/0fbada91e9c3ccf) chore:Updating the version of the gradle-git plugin
- [197d00981b482a5](https://github.com/serenity-bdd/serenity-core/commit/197d00981b482a5) chore:Removed dependency on bintray plugin.
- [400fca7439f69a4](https://github.com/serenity-bdd/serenity-core/commit/400fca7439f69a4) feat: Dropdown.selectByValue()
### v1.0.59
** Commits with examples **
- [6f1628bc721463c](https://github.com/serenity-bdd/serenity-core/commit/6f1628bc721463c) Fixed #87
- [395a9a64e193991](https://github.com/serenity-bdd/serenity-core/commit/395a9a64e193991) Fixes unit tests - nullpointer exception fix when system property webdriver.remote.driver is not set
- [cca6cd03b475dbd](https://github.com/serenity-bdd/serenity-core/commit/cca6cd03b475dbd) Fix for setting up the remote webdriver capability: webdriver.remote.browser.version
### v1.0.58
** Commits with examples **
- [b06c39978f06dad](https://github.com/serenity-bdd/serenity-core/commit/b06c39978f06dad) Refactored tests
- [8e8b01a5fd49895](https://github.com/serenity-bdd/serenity-core/commit/8e8b01a5fd49895) Fixeds #81
- [5b16d86c86702cd](https://github.com/serenity-bdd/serenity-core/commit/5b16d86c86702cd) Fixed #79
### v1.0.57
** Commits with examples **
- [d3777295f2efd74](https://github.com/serenity-bdd/serenity-core/commit/d3777295f2efd74) Performance improvements
- [54529c12066cd60](https://github.com/serenity-bdd/serenity-core/commit/54529c12066cd60) Fixed timeout issues with waitForAbsence* methods
### v1.0.56
** Commits with examples **
- [4350090ac6ec609](https://github.com/serenity-bdd/serenity-core/commit/4350090ac6ec609) Fixed an issue with reporting RestAssured assertion failures.
### v1.0.54
** Commits with examples **
- [fb614fb2bc5bce0](https://github.com/serenity-bdd/serenity-core/commit/fb614fb2bc5bce0) Fixed some timout issues
- [75047a1b8d6fcda](https://github.com/serenity-bdd/serenity-core/commit/75047a1b8d6fcda) Handle null-value parameters more elegantly.
- [7bc74def0bf22fe](https://github.com/serenity-bdd/serenity-core/commit/7bc74def0bf22fe) feat: Added support for Spring meta-annotations for @ContextConfiguration and @ContextHierarchy
- [05c4283ddeedcc9](https://github.com/serenity-bdd/serenity-core/commit/05c4283ddeedcc9) feat: Add support for Spring @ContextHierarchy annotations
### v1.0.53
** Commits with examples **
- [4aee7bb76735218](https://github.com/serenity-bdd/serenity-core/commit/4aee7bb76735218) Temporarily disable some tests with environment-specific issues
- [778ea0699595172](https://github.com/serenity-bdd/serenity-core/commit/778ea0699595172) More refactoring tests
- [11b84b726006eff](https://github.com/serenity-bdd/serenity-core/commit/11b84b726006eff) More refactoring tests
- [1a4268c8749d0f6](https://github.com/serenity-bdd/serenity-core/commit/1a4268c8749d0f6) More refactoring tests
- [45d11b56f149692](https://github.com/serenity-bdd/serenity-core/commit/45d11b56f149692) Refactoring tests
- [1345adf38741118](https://github.com/serenity-bdd/serenity-core/commit/1345adf38741118) Refactoring tests
- [1e636a6e0192ade](https://github.com/serenity-bdd/serenity-core/commit/1e636a6e0192ade) Refactoring tests
- [eed9a7c1b837c4d](https://github.com/serenity-bdd/serenity-core/commit/eed9a7c1b837c4d) Refactoring tests
- [2a4a06f28a3a92b](https://github.com/serenity-bdd/serenity-core/commit/2a4a06f28a3a92b) Better reporting of exceptions (fixes #71)
- [259741557e10c1f](https://github.com/serenity-bdd/serenity-core/commit/259741557e10c1f) Handle recursive parameters correctly (#66)
- [6421a4ccd0b4964](https://github.com/serenity-bdd/serenity-core/commit/6421a4ccd0b4964) Added better support for reporting exceptions
 We now support reporting exceptions with a zero-parameter constructor as well as a single-parameter constructor. 
### v1.0.52
** Commits with examples **
- [0a7fdeacf6a3f4a](https://github.com/serenity-bdd/serenity-core/commit/0a7fdeacf6a3f4a) Modifying screenshot code to work better with Windows (see #69)
- [b184b84b1d9701e](https://github.com/serenity-bdd/serenity-core/commit/b184b84b1d9701e) Modifying screenshot code to work better with Windows (see #69)
### v1.0.51
** Commits with examples **
- [a100646a8697ec4](https://github.com/serenity-bdd/serenity-core/commit/a100646a8697ec4) Updated to Selenium 2.46.0
- [dac9fead420ecb8](https://github.com/serenity-bdd/serenity-core/commit/dac9fead420ecb8) Resolved dependency conflict
- [d0d500c06511a93](https://github.com/serenity-bdd/serenity-core/commit/d0d500c06511a93) Attempt to fix #69
 Issue #69 looks like an OS/filesystem-specific issue related to Java 7 atomic copies. This version uses REPLACE_EXISTING instead of ATOMIC_MOVE. 
- [5dfcc1a4ec89a09](https://github.com/serenity-bdd/serenity-core/commit/5dfcc1a4ec89a09) Updated to Selenium 2.46.0
- [6e7255dc2c22bfc](https://github.com/serenity-bdd/serenity-core/commit/6e7255dc2c22bfc) Deprecate SpringIntegration.
 Add SpringIntegrationMethodRule and SpringIntegrationClassRule, as well as the utility runner SpringIntegrationSerenityRunner, which conveniently automatically adds the aforementioned rules. 
 (Note that some of the main code and test code for the above new classes were originally written in Java 8 and used method references, lambdas and java.util.function.*. To get Java 7 support, these has been replaced by interfaces and anonymous inner classes, but if the project ever moves to Java 8, it is recommended that these are replaced once again). 
- [e38147cc49d8c86](https://github.com/serenity-bdd/serenity-core/commit/e38147cc49d8c86) Moved the tests in serenity-junit that depended on serenity-spring, into serenity-spring, so serenity-junit no longer depends on serenity-spring.
 This is in preparation for an upcoming commit - Not doing this would cause a circular dependency between serenity-junit and serenity-spring. 
### v1.0.50
** Commits with examples **
- [6edddb2d16a2796](https://github.com/serenity-bdd/serenity-core/commit/6edddb2d16a2796) Fixed incorrect timeout issue
- [a5c86db27b7657e](https://github.com/serenity-bdd/serenity-core/commit/a5c86db27b7657e) Refactored unit tests for more clarity
### v1.0.49
** Commits with examples **
- [08aba9be2f264cc](https://github.com/serenity-bdd/serenity-core/commit/08aba9be2f264cc) Fixed a minor formatting issue for JBehave embedded tables.
### v1.0.48
** Commits with examples **
- [2e74fdf36e9c37c](https://github.com/serenity-bdd/serenity-core/commit/2e74fdf36e9c37c) Simplified some tests
- [ebb84712cf92e62](https://github.com/serenity-bdd/serenity-core/commit/ebb84712cf92e62) Refactoring some old multi-select code
- [bf01941c99a7857](https://github.com/serenity-bdd/serenity-core/commit/bf01941c99a7857) Refactoring multiple select code
- [8835d57485f46a8](https://github.com/serenity-bdd/serenity-core/commit/8835d57485f46a8) Harmonized test data
- [95f84a18ec27e43](https://github.com/serenity-bdd/serenity-core/commit/95f84a18ec27e43) JUnit tests using the &#39;expected&#39; attribute are not supported.
- [0dd7d28dbc0a255](https://github.com/serenity-bdd/serenity-core/commit/0dd7d28dbc0a255) Fixed a bug related to deriving requirements structures from Cucumber feature files.
- [35250bdb902423f](https://github.com/serenity-bdd/serenity-core/commit/35250bdb902423f) Made the reporting a bit more robust
 Correctly cater for exceptions without an error message. 
- [d4404c10e741ea0](https://github.com/serenity-bdd/serenity-core/commit/d4404c10e741ea0) Fixed #65 - temporary screenshots not deleted
- [28b9b7bfd02d007](https://github.com/serenity-bdd/serenity-core/commit/28b9b7bfd02d007) Fixed #61: issue with path checks on remote appium server
- [ad83c2afa1652ac](https://github.com/serenity-bdd/serenity-core/commit/ad83c2afa1652ac) Display full screenshots in the slideshow view.
- [a47b0aea9f58fe1](https://github.com/serenity-bdd/serenity-core/commit/a47b0aea9f58fe1) Fixed #64: issue with resetting implicit timeouts
- [a2d03c8dbf1fcb0](https://github.com/serenity-bdd/serenity-core/commit/a2d03c8dbf1fcb0) Fix for THUCYDIDES-253
- [23af5a66522cc35](https://github.com/serenity-bdd/serenity-core/commit/23af5a66522cc35) Added basic support for RestAssured.
 You can now add the serenity-rest-assured module to have tight integration with Rest Assured for testing REST web services. Serenity provides a wrapper around the RestAssured methods that reports on the REST queries sent and the responses recieved. Use the SerenityRest.rest() method as a starting point, e.g. 
 ```` 
 rest().given().contentType(&quot;application/json&quot;).content(jsonPet).post(&quot;http://petstore.swagger.io/v2/pet&quot;); 
 rest().get(&quot;http://petstore.swagger.io/v2/pet/{id}&quot;, pet.getId()).then().statusCode(200) 
 .and().body(&quot;name&quot;, equalTo(pet.getName())); 
 ```` 
- [f0952b4b4245ef2](https://github.com/serenity-bdd/serenity-core/commit/f0952b4b4245ef2) Renamed &#39;core&#39; to &#39;serenity-core&#39;
- [6ab197f15acdd0f](https://github.com/serenity-bdd/serenity-core/commit/6ab197f15acdd0f) Inject EnvironmentVariables fields in PageObjects
- [9ba8c65f64e1346](https://github.com/serenity-bdd/serenity-core/commit/9ba8c65f64e1346) Minor formatting fixes in the reports.
### v1.0.47
** Commits with examples **
- [d296863429cfdab](https://github.com/serenity-bdd/serenity-core/commit/d296863429cfdab) Support for detection of feature file directories.
- [897226ef47f7828](https://github.com/serenity-bdd/serenity-core/commit/897226ef47f7828) Added containsElements() methods to the PageObject class.
- [ba4153da4c89e33](https://github.com/serenity-bdd/serenity-core/commit/ba4153da4c89e33) Improved automatic detection of file-system requirements hierarchies.
 Looks for JBehave or Cucumber feature files and derives the 
 corresponding requirements structure based on the depth of the 
 requirements directories. 
- [ac5ff92cbc9e82e](https://github.com/serenity-bdd/serenity-core/commit/ac5ff92cbc9e82e) Ensure that the correct stack trace is displayed in the reports
- [81fd9206bafb849](https://github.com/serenity-bdd/serenity-core/commit/81fd9206bafb849) Removed system properties from the JUnit results to save space.
- [39d059a4b103ea1](https://github.com/serenity-bdd/serenity-core/commit/39d059a4b103ea1) Added a hasClass() method to the WebElementFacade
 This method is a convenient way to check whether a web element has a 
 particular CSS class. 
- [b4fbf0017c6b530](https://github.com/serenity-bdd/serenity-core/commit/b4fbf0017c6b530) Fixed a bug that caused the screenshots to not always be taken correctly.
- [ef5aebc607c0df5](https://github.com/serenity-bdd/serenity-core/commit/ef5aebc607c0df5) Fixed a bug in the JUnit parameterized reports
 Ensure that errors are correctly reported in JUnit parameterized reports. 
- [faabd32b9da94de](https://github.com/serenity-bdd/serenity-core/commit/faabd32b9da94de) Refactoring and improving the JUnit test reports
- [17466a54578f563](https://github.com/serenity-bdd/serenity-core/commit/17466a54578f563) Display the stack trace for failing tests in the reports
- [2c7b976d4323e39](https://github.com/serenity-bdd/serenity-core/commit/2c7b976d4323e39) Fixed a bug preventing requirements to be loaded from the filesystem with JBehave.
- [bdc3c68d6bf902c](https://github.com/serenity-bdd/serenity-core/commit/bdc3c68d6bf902c) Serenity now generates JUnit-compatible XML reports.
 These reports have the SERENITY-JUNIT prefix. 
- [036b26b9ae631f4](https://github.com/serenity-bdd/serenity-core/commit/036b26b9ae631f4) Refactoring some tests
- [b810e490feb06ac](https://github.com/serenity-bdd/serenity-core/commit/b810e490feb06ac) Improved the consistency of requirements reporting for JUnit tests.
- [da5c2b71bef30c1](https://github.com/serenity-bdd/serenity-core/commit/da5c2b71bef30c1) Fixed an issue where the tests hang if you call Javascript after a failing step.
- [a549ef00739f185](https://github.com/serenity-bdd/serenity-core/commit/a549ef00739f185) Fixed a bug where tests hung if an invalid selector was used in a waitFor expression.
- [f1ebd7ab77f7b60](https://github.com/serenity-bdd/serenity-core/commit/f1ebd7ab77f7b60) Fixed #49 - sysinfo for build report doesn&#39;t support values with spaces
- [27abd5ccdb9869e](https://github.com/serenity-bdd/serenity-core/commit/27abd5ccdb9869e) Improved error reporting and performance.
- [d5dfc1ea82b7954](https://github.com/serenity-bdd/serenity-core/commit/d5dfc1ea82b7954) Fixed an issue that prevented screenshots from being taken correctly in Cucumber scenarios
- [6bb343b89f02f85](https://github.com/serenity-bdd/serenity-core/commit/6bb343b89f02f85) Refactored some unit tests
- [ace9f68089764dd](https://github.com/serenity-bdd/serenity-core/commit/ace9f68089764dd) Fixed bug that prevents the arrow keys working in the screenshot slideshow on webkit browsers
- [3414969576f7c76](https://github.com/serenity-bdd/serenity-core/commit/3414969576f7c76) Only process a new screenshot if an existing one doesn&#39;t already exist.
- [7d969e88d54fc0c](https://github.com/serenity-bdd/serenity-core/commit/7d969e88d54fc0c) Allow EnvironmentVariables and SystemConfiguration fields to be
 injected into JUnit tests. 
- [413d8398ede5b58](https://github.com/serenity-bdd/serenity-core/commit/413d8398ede5b58) Reformatting and tidying up imports
- [66d334368720385](https://github.com/serenity-bdd/serenity-core/commit/66d334368720385) Fixed formatting error in the screenshots
### v1.0.46
** Commits with examples **
- [657232a147988a8](https://github.com/serenity-bdd/serenity-core/commit/657232a147988a8) Test refactoring
- [137c534cdfb84b0](https://github.com/serenity-bdd/serenity-core/commit/137c534cdfb84b0) Unit test refactoring
- [c8ab82bc59925ba](https://github.com/serenity-bdd/serenity-core/commit/c8ab82bc59925ba) General refactoring
- [5705bc2b8287608](https://github.com/serenity-bdd/serenity-core/commit/5705bc2b8287608) Support Cucumber feature files written in other languages.
- [8fb2e5e5e0b8204](https://github.com/serenity-bdd/serenity-core/commit/8fb2e5e5e0b8204) Better error reporting for errors around the @DefaultUrl definitions for Page Objects.
- [5205c75874d5344](https://github.com/serenity-bdd/serenity-core/commit/5205c75874d5344) Added better error reporting if a groovy expression in the build info properties was incorrect
 Better error handling for Groovy expressions used in the “sysinfo.*” 
 system properties that appear in the build info page. 
### v1.0.45
** Commits with examples **
- [7848aaa63808598](https://github.com/serenity-bdd/serenity-core/commit/7848aaa63808598) Refactoring and improving the unit tests.
- [7586862312bb43a](https://github.com/serenity-bdd/serenity-core/commit/7586862312bb43a) Support for PhantomJS 1.2.1
- [42884b1685a5b2d](https://github.com/serenity-bdd/serenity-core/commit/42884b1685a5b2d) Don&#39;t display the browser icon for non-web tests.
 Distinguish among Serenity Web Tests (Selenium) and Serenity Non-Web Test (#41) 
- [d054c41b4ff58b9](https://github.com/serenity-bdd/serenity-core/commit/d054c41b4ff58b9) Fixed issue with uploading files from the Windows file system.
- [c16591002d6d237](https://github.com/serenity-bdd/serenity-core/commit/c16591002d6d237) feat: added the possiblity to wait for a CSS or XPath expression from a chained expression.
- [daacd77e56937db](https://github.com/serenity-bdd/serenity-core/commit/daacd77e56937db) feat: Custom build properties are reported in a more human-readable way in the build info screen.
- [4e17cef7fc39428](https://github.com/serenity-bdd/serenity-core/commit/4e17cef7fc39428) Added the &#39;feature.file.language&#39; to support I18N feature files
 Narrative text can now be read from non-English feature files, by setting the &#39;feature.file.language&#39; system property. 
- [e7ae87e1fd29953](https://github.com/serenity-bdd/serenity-core/commit/e7ae87e1fd29953) Fix problem with uploading file on Windows. Changed creation of file path (if file in classpath)
- [2ec6dd245337d4a](https://github.com/serenity-bdd/serenity-core/commit/2ec6dd245337d4a) ensure unused threads are terminated and removed from executor pool
### v1.0.44
** Commits with examples **
- [e5d04ef4380fc77](https://github.com/serenity-bdd/serenity-core/commit/e5d04ef4380fc77) feat: Added a total time in the test results report.
- [5e446cb122eb203](https://github.com/serenity-bdd/serenity-core/commit/5e446cb122eb203) feat: Added a total time in the test results report.
- [3838821d026b929](https://github.com/serenity-bdd/serenity-core/commit/3838821d026b929) feat: You can now automatically inject EnvironmentVariables and Configuration variables into your step libraries, simply by declaring a variable of the corresponding type.
### v1.0.43
** Commits with examples **
- [85f58025c933967](https://github.com/serenity-bdd/serenity-core/commit/85f58025c933967) Changed the default page size for the test results to 50.
### v1.0.42
** Commits with examples **
- [33ff1a16031cb98](https://github.com/serenity-bdd/serenity-core/commit/33ff1a16031cb98) Allows explicit waits on web elements in a page
 For example: 
 withTimeoutOf(5, TimeUnit.SECONDS).waitFor(facebookIcon).click() 
### v1.0.41
** Commits with examples **
- [b497a1db7698833](https://github.com/serenity-bdd/serenity-core/commit/b497a1db7698833) Implemented the timeoutInSeconds attribute on the FindBy annotation.
- [d8ccfdabf6a5952](https://github.com/serenity-bdd/serenity-core/commit/d8ccfdabf6a5952) Implemented the timeoutInSeconds attribute on the FindBy annotation.
### v1.0.40
** Commits with examples **
- [e7235f713c2d379](https://github.com/serenity-bdd/serenity-core/commit/e7235f713c2d379) Refactored wait logic to use distinct values for implicit waits and wait-for waits.
- [0fa63e2aba5951d](https://github.com/serenity-bdd/serenity-core/commit/0fa63e2aba5951d) Added containsElements() and shouldContainElements() methods to WebElementFacade
- [9d9c5a4b6a19c4f](https://github.com/serenity-bdd/serenity-core/commit/9d9c5a4b6a19c4f) Added a convenience method to allow more fluent waitFor() constructs
### v1.0.39
** Commits with examples **
- [ac3de4e6f2f409b](https://github.com/serenity-bdd/serenity-core/commit/ac3de4e6f2f409b) tests: hardeding the timeout tests
- [b29b7cc6ce97ee9](https://github.com/serenity-bdd/serenity-core/commit/b29b7cc6ce97ee9) feature: Added support for a waitUntilClickable() method on web elements
- [82d1ab1c848b7d3](https://github.com/serenity-bdd/serenity-core/commit/82d1ab1c848b7d3) tests: test hardening
- [2eca74a07bd6db6](https://github.com/serenity-bdd/serenity-core/commit/2eca74a07bd6db6) fix: Fixed a bug in reading the requirements from the file system.
- [9a6c99dcc3e1949](https://github.com/serenity-bdd/serenity-core/commit/9a6c99dcc3e1949) fix: Fixed a bug in reading the requirements from the file system.
- [38280276b961e60](https://github.com/serenity-bdd/serenity-core/commit/38280276b961e60) fix: Fixed a bug in reading the requirements from the file system.
- [73ce792b29c26b4](https://github.com/serenity-bdd/serenity-core/commit/73ce792b29c26b4) Removed redundant test
- [dbddf6df434355f](https://github.com/serenity-bdd/serenity-core/commit/dbddf6df434355f) test: Temporarily disabling a test that doesn&#39;t work on the build server pending further investigation
- [5a46d718876a96a](https://github.com/serenity-bdd/serenity-core/commit/5a46d718876a96a) test: Use phantomjs to check implicit timeouts more realisticly
- [204900f5f48211a](https://github.com/serenity-bdd/serenity-core/commit/204900f5f48211a) Rewrote much of the timeout APIs
### v1.0.38
** Commits with examples **
- [0c23f3a8c26b06e](https://github.com/serenity-bdd/serenity-core/commit/0c23f3a8c26b06e) test: Temporarily disabling a test that doesn&#39;t work on the build server pending further investigation
- [536bfdf46cac5b0](https://github.com/serenity-bdd/serenity-core/commit/536bfdf46cac5b0) test: Use phantomjs to check implicit timeouts more realisticly
- [9e653329dd691a5](https://github.com/serenity-bdd/serenity-core/commit/9e653329dd691a5) Added tests to doument implicit wait behavior
- [4bfdb9133300e0e](https://github.com/serenity-bdd/serenity-core/commit/4bfdb9133300e0e) test: Added sample JSON test data
- [219441fb70fb4b9](https://github.com/serenity-bdd/serenity-core/commit/219441fb70fb4b9) test: Added sample JSON test data
- [cd09406dcb34a96](https://github.com/serenity-bdd/serenity-core/commit/cd09406dcb34a96) Added test data for a sample pending report
- [c191b5a2b3d0a8c](https://github.com/serenity-bdd/serenity-core/commit/c191b5a2b3d0a8c) Added test data for a sample pending report
- [66801ffbbc769e4](https://github.com/serenity-bdd/serenity-core/commit/66801ffbbc769e4) Added test data for a sample pending report
- [ac60be617fe6dd1](https://github.com/serenity-bdd/serenity-core/commit/ac60be617fe6dd1) Fixed an issue with Cucumber requirements reporting when the name of the feature differs from the name of the feature file.
- [a6d6cc62c576351](https://github.com/serenity-bdd/serenity-core/commit/a6d6cc62c576351) Fixed an issue with Cucumber requirements reporting when the name of the feature differs from the name of the feature file.
- [d2a20188ab24fd4](https://github.com/serenity-bdd/serenity-core/commit/d2a20188ab24fd4) Update WhenLoadingTestDataFromACSVFile.java
 Added all possible parameters for CSVReader to be able to parse special chars like \n \t ... 
- [8043809da640f99](https://github.com/serenity-bdd/serenity-core/commit/8043809da640f99) Update WhenLoadingTestDataFromACSVFile.java
 Added all possible parameters for CSVReader to be able to parse special chars like \n \t ... 
- [aa1c3ed0fa00fc7](https://github.com/serenity-bdd/serenity-core/commit/aa1c3ed0fa00fc7) Update CSVTestDataSource.java
 Added all possible parameters for CSVReader to be able to parse special chars like \n \t ... 
- [df893d20c253dbc](https://github.com/serenity-bdd/serenity-core/commit/df893d20c253dbc) Update CSVTestDataSource.java
 Added all possible parameters for CSVReader to be able to parse special chars like \n \t ... 
- [cd9d78657ed78ab](https://github.com/serenity-bdd/serenity-core/commit/cd9d78657ed78ab) Fixed an issue in the reports where pending test results were not being accurately reported in the pie charts.
- [326a643ba2bcb0d](https://github.com/serenity-bdd/serenity-core/commit/326a643ba2bcb0d) Fixed an issue in the reports where pending test results were not being accurately reported in the pie charts.
### v1.0.37
** Commits with examples **
- [b3d38fb9a30fd74](https://github.com/serenity-bdd/serenity-core/commit/b3d38fb9a30fd74) test:Made a unit test more readable
- [403003dfbac409d](https://github.com/serenity-bdd/serenity-core/commit/403003dfbac409d) Refactored the dependencies to use both the group and the module names in exclusions, to make the Maven Enforcer plugin happy
- [9d25a1aa46fcfe3](https://github.com/serenity-bdd/serenity-core/commit/9d25a1aa46fcfe3) Refactored the dependencies to use both the group and the module names in exclusions, to make the Maven Enforcer plugin happy
- [fe952b944bf628d](https://github.com/serenity-bdd/serenity-core/commit/fe952b944bf628d) Fixed an issue that had broken the async timeout behavior in the setScriptTimeout() method
### v1.0.36
** Commits with examples **
- [d21e03e66f56d86](https://github.com/serenity-bdd/serenity-core/commit/d21e03e66f56d86) Standardized the Groovy version used throughout the build to 2.3.6
- [e8c1a874c9030db](https://github.com/serenity-bdd/serenity-core/commit/e8c1a874c9030db) Updated to Selenium 2.45.0
- [71fcf22e7fe7693](https://github.com/serenity-bdd/serenity-core/commit/71fcf22e7fe7693) test: Refactored a few tests to reduce sporadic errors
- [3026d248d044014](https://github.com/serenity-bdd/serenity-core/commit/3026d248d044014) test: ensured that HTMLUnit tests closed the drivers to avoid memory leaks during the build.
### v1.0.35
** Commits with examples **
- [d7f4cd3ab1d16d1](https://github.com/serenity-bdd/serenity-core/commit/d7f4cd3ab1d16d1) fix: Fixed an issue in which tests were slowed down after a failing step because Serenity continued to try to take screenshots
### v1.0.34
** Commits with examples **
- [e20146db9d8e882](https://github.com/serenity-bdd/serenity-core/commit/e20146db9d8e882) test:Updated some unit tests
- [2d48ba34363f7e1](https://github.com/serenity-bdd/serenity-core/commit/2d48ba34363f7e1) test:Updated some unit tests
- [b55c8cd17404b9a](https://github.com/serenity-bdd/serenity-core/commit/b55c8cd17404b9a) feat: Distinguish between element-level timing and &quot;wait-for&quot;-style timing.
- [2cb5e77f4aa71a6](https://github.com/serenity-bdd/serenity-core/commit/2cb5e77f4aa71a6) fix: Fixed a bug where the reports fail to generate if there are skipped test results in the outcomes.
- [924764f8f9f38eb](https://github.com/serenity-bdd/serenity-core/commit/924764f8f9f38eb) feat: Improved the readability of parameters in the screenshot pages.
- [a1dba09cd2737da](https://github.com/serenity-bdd/serenity-core/commit/a1dba09cd2737da) feat: You can now distinguish between AJAX element waits (defaults to 500 ms) and explicit fluent waits (which default to 5 seconds)
### v1.0.33
** Commits with examples **
- [4931d367a7d3e80](https://github.com/serenity-bdd/serenity-core/commit/4931d367a7d3e80) fix: Tidied up dependencies used by the other serenity modules
- [23d27526cd201f3](https://github.com/serenity-bdd/serenity-core/commit/23d27526cd201f3) fix: Tidied up dependencies used by the other serenity modules
- [931e476b086f4a0](https://github.com/serenity-bdd/serenity-core/commit/931e476b086f4a0) fix: Tidied up dependencies used by the other serenity modules
### v1.0.32
** Commits with examples **
- [93b836f8f2a811e](https://github.com/serenity-bdd/serenity-core/commit/93b836f8f2a811e) fix: fixed an issue loading the JSON test reports during aggregate report generation.
- [5894af6eb234394](https://github.com/serenity-bdd/serenity-core/commit/5894af6eb234394) fix: Removed dependency conflicts in the Gradle build.
- [388304241495e0c](https://github.com/serenity-bdd/serenity-core/commit/388304241495e0c) feat: nested page objects i.e. widget objects
 WidgetObject: reusable page fragment with a nested search context implied by the Composition pattern.  This feature was requested here: 
 https://groups.google.com/forum/#!topic/thucydides-users/-SiQwD86W8I 
 https://groups.google.com/forum/#!topic/thucydides-users/01oNgOD9TnY 
 See attached unit tests for usage examples. 
- [26f09b00e71da04](https://github.com/serenity-bdd/serenity-core/commit/26f09b00e71da04) Fixed issue #23
- [072b8de691e74fc](https://github.com/serenity-bdd/serenity-core/commit/072b8de691e74fc) removed duplicate test model
- [7ba089050433c51](https://github.com/serenity-bdd/serenity-core/commit/7ba089050433c51) feat: Lists of WebElementFacade and subtypes as PageObject members.
- [7094f8dc6dd6bae](https://github.com/serenity-bdd/serenity-core/commit/7094f8dc6dd6bae) Fixed a bug where if a null value was stored in the Serenity session after a failing step, a null pointer exception was thrown.
### v1.0.31
** Commits with examples **
- [e78dd2cfdd98e23](https://github.com/serenity-bdd/serenity-core/commit/e78dd2cfdd98e23) Added support for displaying Saucelabs configuration in the build info screen.
- [56f672a7f8d5941](https://github.com/serenity-bdd/serenity-core/commit/56f672a7f8d5941) Made table formatting more robust by providing support for unicode brackets and new line chars.
- [4b6696672cfa002](https://github.com/serenity-bdd/serenity-core/commit/4b6696672cfa002) Removed redundant Jackson adaptor classes
- [11b988b4948ee76](https://github.com/serenity-bdd/serenity-core/commit/11b988b4948ee76) Use Durations rather than longs and ints to handle timeout values, in order to avoid coding errors, make the code clearer, and as a basis for more flexible timeout configuration.
### v1.0.30
** Commits with examples **
- [5f4b87c9b97869e](https://github.com/serenity-bdd/serenity-core/commit/5f4b87c9b97869e) Use Java NIO to copy report resources.
- [826c30fb0ea0c99](https://github.com/serenity-bdd/serenity-core/commit/826c30fb0ea0c99) Refactored the PageObject class for better backward compatibility.
### v1.0.29
** Commits with examples **
- [26cce2dce32adc6](https://github.com/serenity-bdd/serenity-core/commit/26cce2dce32adc6) Made a test cross-platform
- [fe1ab3e2ce34859](https://github.com/serenity-bdd/serenity-core/commit/fe1ab3e2ce34859) Added a page to the reports containing system and configuration properties and browser capabilities for a given test run.
 The browser used for each test is also recorded and displayed as an icon on the test report pages. 
 You can also add your own custom fields into the build information page. You do this by adding properties with the &quot;sysinfo&quot; prefix to your serenity.properties file. These variables take Groovy expressions, which will be evaluated when the report is run, e.g: 
 sysinfo.theAnswer = 6*7 
 sysinfo.homeDir = System.getenv(&quot;HOME&quot;) 
- [828c57af675ff9d](https://github.com/serenity-bdd/serenity-core/commit/828c57af675ff9d) Made the JSON tests a bit more robust
- [8fee3ad84895083](https://github.com/serenity-bdd/serenity-core/commit/8fee3ad84895083) Chrome no longer opens a new window when you specify the browser size.
 Also, the browser is now automatically positioned in the top left hand corner of the screen. 
 Signed-off-by: John Ferguson Smart &lt;john.smart@wakaleo.com&gt; 
- [9784811403dd789](https://github.com/serenity-bdd/serenity-core/commit/9784811403dd789) Migrated the PageObject class to the serenitybdd namespace.
 Signed-off-by: John Ferguson Smart &lt;john.smart@wakaleo.com&gt; 
- [8b360c130452d8c](https://github.com/serenity-bdd/serenity-core/commit/8b360c130452d8c) Removed Jackson dependencies
- [7020e788a36a4c2](https://github.com/serenity-bdd/serenity-core/commit/7020e788a36a4c2) Removing Jackson
- [f4ccaf8310b5ddf](https://github.com/serenity-bdd/serenity-core/commit/f4ccaf8310b5ddf) Fixed a bug that prevented the proper use of commands like &#39;webdriver.manage().window().setSize(new Dimension(1600, 1200));&#39;
### v1.0.27
** Commits with examples **
- [b52b55a39a9d501](https://github.com/serenity-bdd/serenity-core/commit/b52b55a39a9d501) Now you can use the -Dserenity.dry.run=true option to skip step executions - useful when testing JBehave or Cucumber step definitions
### v1.0.26
** Commits with examples **
- [068315f4f0e63d4](https://github.com/serenity-bdd/serenity-core/commit/068315f4f0e63d4) Performance improvements: forces WebDriver to force an immediate response for findElements() calls if no matching elements are found, and some other minor improvements.
 Also improved step logging to include the test class and method as well as the step name. 
 Signed-off-by: John Ferguson Smart &lt;john.smart@wakaleo.com&gt; 
- [f9d996950d02e31](https://github.com/serenity-bdd/serenity-core/commit/f9d996950d02e31) Made the log messages for each step include the calling class and method.
 Signed-off-by: John Ferguson Smart &lt;john.smart@wakaleo.com&gt; 
- [afaf0b947f97a8c](https://github.com/serenity-bdd/serenity-core/commit/afaf0b947f97a8c) Fix to remove &#39;Session ID is null. Using WebDriver after calling quit()?&#39; messages appearing when the tests are run in threads
- [a2d3a0f17b4ad20](https://github.com/serenity-bdd/serenity-core/commit/a2d3a0f17b4ad20) Refactored optional Spring dependencies into the serenity-spring module - include this module if you want Serenity to honor Spring annotations and dependency injection
- [c9f95050aadcd98](https://github.com/serenity-bdd/serenity-core/commit/c9f95050aadcd98) Upgrade javassist version to match transitive dep. #16
 core&#39;s version was 3.9.0.GA; reflections version is 3.12.1.GA 
- [80e0099cf475874](https://github.com/serenity-bdd/serenity-core/commit/80e0099cf475874) Working again after serenity package rename
### v1.0.25
** Commits with examples **
- [89f6ca56633ed1c](https://github.com/serenity-bdd/serenity-core/commit/89f6ca56633ed1c) Provide better support for step-level error reporting in Cucumber.
- [52e64aef5ebbe28](https://github.com/serenity-bdd/serenity-core/commit/52e64aef5ebbe28) Tidied up some dependencies.
- [003791a889e2988](https://github.com/serenity-bdd/serenity-core/commit/003791a889e2988) Extracted dependency injection into an external module, to make it easier to add additional dependency injection modules later
- [3144ad12699cd6a](https://github.com/serenity-bdd/serenity-core/commit/3144ad12699cd6a) Upgrade groovy-all version for transitive convergence #16.
- [392bc01b88be7b4](https://github.com/serenity-bdd/serenity-core/commit/392bc01b88be7b4) Upgrade SLF4J version for transitive convergence #16.
- [099d1189d1c5d0c](https://github.com/serenity-bdd/serenity-core/commit/099d1189d1c5d0c) core build: exclude transitive deps with convergence problems. #16
 Declare additional transitive deps. 
- [197fab566647c12](https://github.com/serenity-bdd/serenity-core/commit/197fab566647c12) Top build: declare transitives as deps. #16
- [22d5395e9df2cbc](https://github.com/serenity-bdd/serenity-core/commit/22d5395e9df2cbc) Top build: fail fast on dependency convergence problems. #16
 Added &quot;force version&quot; on transitive versions with convergence 
 problems. 
 Issue: While this works to keep gradle build clean, it doesn&#39;t 
 affect the generated POM/install for clients. 
- [7a267aa8399a3dd](https://github.com/serenity-bdd/serenity-core/commit/7a267aa8399a3dd) Build: Add plugins that help with dep versions. #16
 - project-report: 
 - gradlew htmlDependencyReport creates HTML dep report that shows 
 which deps the build managed to different version. 
 - com.github.ben-manes.versions: 
 - gradlew dependencyUpdates shows deps with new versions 
- [70325bb74775cb3](https://github.com/serenity-bdd/serenity-core/commit/70325bb74775cb3) Upgrade commons-lang3 to htmlunit&#39;s dep version. #16
 HtmlUnit uses 3.3.2, Serenity was using 3.1. 
- [ceb0c1d103411a9](https://github.com/serenity-bdd/serenity-core/commit/ceb0c1d103411a9) Upgrade htmlunit to Selenium&#39;s dep version. #16
 Selenium uses 2.15, Serenity was using 2.9. 
### v1.0.24
** Commits with examples **
- [d9a768af4b3eb2a](https://github.com/serenity-bdd/serenity-core/commit/d9a768af4b3eb2a) Release notes are now triggered manually before the release
- [c36529114af5daa](https://github.com/serenity-bdd/serenity-core/commit/c36529114af5daa) Updated release notest
- [7c429c02e9f8522](https://github.com/serenity-bdd/serenity-core/commit/7c429c02e9f8522) Migrated the default output directory to target/site/serenity
- [82b98664486be5d](https://github.com/serenity-bdd/serenity-core/commit/82b98664486be5d) Migrated the default output directory to target/site/serenity
- [97156bd6c56b571](https://github.com/serenity-bdd/serenity-core/commit/97156bd6c56b571) Added support for better Cucumber reporting
- [5ea5e898b1bcab7](https://github.com/serenity-bdd/serenity-core/commit/5ea5e898b1bcab7) Updated release notes
- [88dbe9c8342f0d8](https://github.com/serenity-bdd/serenity-core/commit/88dbe9c8342f0d8) Restored release notes
- [9716bc56de482ff](https://github.com/serenity-bdd/serenity-core/commit/9716bc56de482ff) Make sure the release notes are produced dynamically
- [9e9711d48eca8bb](https://github.com/serenity-bdd/serenity-core/commit/9e9711d48eca8bb) Added extra support for handling Cucumber example tables
- [e3ce499a6d4f91e](https://github.com/serenity-bdd/serenity-core/commit/e3ce499a6d4f91e) Simplified dependencies a little
- [7cb2a81cae949bd](https://github.com/serenity-bdd/serenity-core/commit/7cb2a81cae949bd) WIP
- [25e0cd1393bcc92](https://github.com/serenity-bdd/serenity-core/commit/25e0cd1393bcc92) Updated release notes
- [3a71aaea630baf7](https://github.com/serenity-bdd/serenity-core/commit/3a71aaea630baf7) refactor: PageObject still returns thucydides WebElementFacadeImpl so that can be cast to serenitybdd namespace
 This will need to be cleaned up when the thucydides namespace is retired. 
- [f9d713e343d9380](https://github.com/serenity-bdd/serenity-core/commit/f9d713e343d9380) style: fix typo in logging
- [2648daa127fe42d](https://github.com/serenity-bdd/serenity-core/commit/2648daa127fe42d) refactor: Create serenitybdd version of WebElementFacade classes/interfaces
 Deprecate Thucydides versions, but still handle them correctly 
- [2bde33abd91afd7](https://github.com/serenity-bdd/serenity-core/commit/2bde33abd91afd7) refactor: Move tests from thucydides to serenitybdd package
- [7edba47608a800c](https://github.com/serenity-bdd/serenity-core/commit/7edba47608a800c) Improved release notes to avoid empty tags
- [9e47250a7a37d86](https://github.com/serenity-bdd/serenity-core/commit/9e47250a7a37d86) Improved release notes to avoid empty tags
- [948caa8ad7924d4](https://github.com/serenity-bdd/serenity-core/commit/948caa8ad7924d4) Updated release notes
- [71d6c5a562d886d](https://github.com/serenity-bdd/serenity-core/commit/71d6c5a562d886d) Updated the README file to reflect the new commit conventions
- [8208430d61bec12](https://github.com/serenity-bdd/serenity-core/commit/8208430d61bec12) Updated release notes
- [80ee2cfb7f92285](https://github.com/serenity-bdd/serenity-core/commit/80ee2cfb7f92285) chore: Automated the generation of the release notes from the git commits
### v1.0.23
** Commits with examples **
- [8d8b0bf5fb05fce](https://github.com/serenity-bdd/serenity-core/commit/8d8b0bf5fb05fce) You can now use serenity.* instead of thucydides.* system properties. The thucydides.* system properties are still supported, but a warning is printed to the logs.
- [cfaae5a78a36fbb](https://github.com/serenity-bdd/serenity-core/commit/cfaae5a78a36fbb) rename serenity_bdd to serenitybdd
### v1.0.22
** Commits with examples **
- [3443435570d0e97](https://github.com/serenity-bdd/serenity-core/commit/3443435570d0e97) Move junit finder classes to serenity_bdd package
- [7bde2389379fa22](https://github.com/serenity-bdd/serenity-core/commit/7bde2389379fa22) Rename package in demo to serenity_bdd
- [2aa92f97522d705](https://github.com/serenity-bdd/serenity-core/commit/2aa92f97522d705) SerenityRunner and SerenityParameterizedRunner now contain functionality, and Thucydides equivalents merely extend
 Also move a number of helper classes into serenity_bdd package 
- [b94933d99cc7e9f](https://github.com/serenity-bdd/serenity-core/commit/b94933d99cc7e9f) Move JUnit runners to serenity_bdd package
### v1.0.21
** Commits with examples **
- [5fc6c9a9e3e0b7c](https://github.com/serenity-bdd/serenity-core/commit/5fc6c9a9e3e0b7c) Improvements to the reports
- [c31cb4f4b17a086](https://github.com/serenity-bdd/serenity-core/commit/c31cb4f4b17a086) Improvements to the reports
### v1.0.18
** Commits with examples **
- [6ee7578c7e241b6](https://github.com/serenity-bdd/serenity-core/commit/6ee7578c7e241b6) Added better support for comments in feature files, and better formatting in the &#39;Related Tabs&#39; table
- [9b7e9c43d7f6bab](https://github.com/serenity-bdd/serenity-core/commit/9b7e9c43d7f6bab) Hardening unit tests
- [199e60a595c0830](https://github.com/serenity-bdd/serenity-core/commit/199e60a595c0830) Updated reporting, attempt 2
### v1.0.17
** Commits with examples **
- [602eaf8dfe8633e](https://github.com/serenity-bdd/serenity-core/commit/602eaf8dfe8633e) Added tool tips on the &#39;Related Tags&#39; tables
- [a05b31ffb0928e9](https://github.com/serenity-bdd/serenity-core/commit/a05b31ffb0928e9) Undid javascript library updates and added the number of tests for tags on the reports
- [0a272c47a9a49f2](https://github.com/serenity-bdd/serenity-core/commit/0a272c47a9a49f2) Revert &quot;Updated libraries&quot;
 This reverts commit 44ec91e92d90ebc3742a6221f82d1a404b1baa57. 
- [f8f476230acb6e8](https://github.com/serenity-bdd/serenity-core/commit/f8f476230acb6e8) Revert &quot;Update reports to use new libraries&quot;
 This reverts commit f4a75422ecfc46a66fb5ebb617ce808c299a6d4b. 
- [d017a61caa8d820](https://github.com/serenity-bdd/serenity-core/commit/d017a61caa8d820) Revert &quot;Refactoring to facilitate easier migrating to new versions of the libraries&quot;
 This reverts commit 6f12e5389a8499e2f9f9b69478b329f90367d4fb. 
- [a25fed4b5fe3830](https://github.com/serenity-bdd/serenity-core/commit/a25fed4b5fe3830) Revert &quot;Updated excanvas&quot;
 This reverts commit 5d55b1eae5d424b7185ed1aab68ab6f36c53cbf6. 
- [b49d68030bb88d0](https://github.com/serenity-bdd/serenity-core/commit/b49d68030bb88d0) Revert &quot;Updated JavaScript InfoVis Toolkit&quot;
 This reverts commit a3c95dc54f1165c5ea00fcb2719f14a63acba604. 
- [1b62cb0a07240b4](https://github.com/serenity-bdd/serenity-core/commit/1b62cb0a07240b4) Revert &quot;Removed old versions of libraries&quot;
 This reverts commit 7b26344dea3c0ee710ee90fe7040141a6941f97f. 
- [911799b02a2d987](https://github.com/serenity-bdd/serenity-core/commit/911799b02a2d987) Fixed issues with identifying appium driver
- [7b26344dea3c0ee](https://github.com/serenity-bdd/serenity-core/commit/7b26344dea3c0ee) Removed old versions of libraries
- [a3c95dc54f1165c](https://github.com/serenity-bdd/serenity-core/commit/a3c95dc54f1165c) Updated JavaScript InfoVis Toolkit
- [5d55b1eae5d424b](https://github.com/serenity-bdd/serenity-core/commit/5d55b1eae5d424b) Updated excanvas
- [6f12e5389a8499e](https://github.com/serenity-bdd/serenity-core/commit/6f12e5389a8499e) Refactoring to facilitate easier migrating to new versions of the libraries
- [f4a75422ecfc46a](https://github.com/serenity-bdd/serenity-core/commit/f4a75422ecfc46a) Update reports to use new libraries
- [44ec91e92d90ebc](https://github.com/serenity-bdd/serenity-core/commit/44ec91e92d90ebc) Updated libraries
### v1.0.16
** Commits with examples **
- [18d5f80d55e8b83](https://github.com/serenity-bdd/serenity-core/commit/18d5f80d55e8b83) Improved requirement reporting for JUnit (experimental)
- [6376d9951792d7b](https://github.com/serenity-bdd/serenity-core/commit/6376d9951792d7b) This small change makes Serenity compatible with Firefox version 32 or greater
 Guava 18.0 is already specified in Gradle. 
### v1.0.15
** Commits with examples **
- [892b4fe6a8d0fab](https://github.com/serenity-bdd/serenity-core/commit/892b4fe6a8d0fab) Improved reporting of JUnit tests as requirements
### v1.0.14
** Commits with examples **
- [d5f35b9cf08b4e6](https://github.com/serenity-bdd/serenity-core/commit/d5f35b9cf08b4e6) Switched back to JUnit 4.11 due to API incompatibilities with build tools
### v1.0.13
** Commits with examples **
- [7cbe55192607ef2](https://github.com/serenity-bdd/serenity-core/commit/7cbe55192607ef2) The @Pages annotated field in JUnit tests is now optional
- [3d985d15871a528](https://github.com/serenity-bdd/serenity-core/commit/3d985d15871a528) Upgraded to JUnit 4.12
### v1.0.12
** Commits with examples **
- [1290a90ccf2c6c3](https://github.com/serenity-bdd/serenity-core/commit/1290a90ccf2c6c3) Solidified a test
### v1.0.12-rc.1
** Commits with examples **
- [878c2a1edb79d85](https://github.com/serenity-bdd/serenity-core/commit/878c2a1edb79d85) Added better support for radio buttons in the PageObject class
- [0902fc79603d4f0](https://github.com/serenity-bdd/serenity-core/commit/0902fc79603d4f0) Use gradle-git for version and tagging
 === If local repository is dirty 
 -Always builds a SNAPSHOT version. 
 -Will complain that &#39;Stage {} is not one of [SNAPSHOT] allowed for strategy snapshot.&#39; 
 === If local repository is not dirty 
 Set release type using property release.stage. Valid values are: 
 -milestone 
 -rc 
 -final 
 milestone creates a tag with the next version from tag + -milestone.# 
 rc similar, but uses rc. Cannot create a milestone after an rc 
 final creates a version with no endings 
 If want to use ssh authorization, must ensure ssh-agent contains correct key for repository being worked on. 
 If you experience issues, try ssh-add -D to clear identities and add the one identity for the repo in question. 
 The release tags the current commit, and pushes to the remote repository. It does not check if there&#39;s a new commit, so only use it if you really need to. 
 gradle bintrayUpload release -Prelease.stage={milestone|rc|final} 
- [e0a96d7cd7499a4](https://github.com/serenity-bdd/serenity-core/commit/e0a96d7cd7499a4) Fix scm url&#39;s
 All were pointing at project.name, when in fact they all exist in the same 
 serenity-core repository 
- [6d6327665844b25](https://github.com/serenity-bdd/serenity-core/commit/6d6327665844b25) Correct issue with publishing
 Main project doesn&#39;t have anything to deploy, and doesn&#39;t have config. This 
 causes a warning when building the project. 
 Provide the config that is common across all projects in this config file, 
 but no config for the main project is required. 
- [3ee866cd987cfb1](https://github.com/serenity-bdd/serenity-core/commit/3ee866cd987cfb1) Remove unused files
 It would appear that the main project was moved into core sub-directory, and 
 these files didn&#39;t get cleaned up. 
- [ed62753b69b522f](https://github.com/serenity-bdd/serenity-core/commit/ed62753b69b522f) [namespace] Move Find annotations to serenity_bdd namespace
 Create deprecated versions in thucydides namespace but with 2 on name to ensure 
 caught all changes, and returning objects of correct classes. 
 Also kept deprecated versions of tests to ensure old versions still work correctly 
- [47542e1b4cfc29c](https://github.com/serenity-bdd/serenity-core/commit/47542e1b4cfc29c) Made the Ant plugin a bit more robust.
- [c0a1aa089cd72af](https://github.com/serenity-bdd/serenity-core/commit/c0a1aa089cd72af) Moved the ant plugin over to the new Serenity namespace
- [2ed2864f88aaf29](https://github.com/serenity-bdd/serenity-core/commit/2ed2864f88aaf29) [migrate] Move exceptions
- [ad3a486ced855de](https://github.com/serenity-bdd/serenity-core/commit/ad3a486ced855de) [migrate] Move SessionMap
- [d84aeede8457858](https://github.com/serenity-bdd/serenity-core/commit/d84aeede8457858) [rename] Create Serenity namespaced class and move some associated test classes
- [3705ee4ffed330e](https://github.com/serenity-bdd/serenity-core/commit/3705ee4ffed330e) [rename] Create Serenity namespaced class, deprecate Thucydides version and delegate functions
- [8bdaf7db8f1f501](https://github.com/serenity-bdd/serenity-core/commit/8bdaf7db8f1f501) [rename] Move SerenityListeners and create deprecated ThucydidesListeners
- [61cc4d855d5a0ef](https://github.com/serenity-bdd/serenity-core/commit/61cc4d855d5a0ef) Display error messages for ignored steps, so that failing assumption messages are correctly displayed
- [04cace4c7b9b053](https://github.com/serenity-bdd/serenity-core/commit/04cace4c7b9b053) Updated banners
- [be15eb47c729538](https://github.com/serenity-bdd/serenity-core/commit/be15eb47c729538) Move Serenity to new package
- [581dd4753b647b3](https://github.com/serenity-bdd/serenity-core/commit/581dd4753b647b3) Rename main class to reflect new project name, and deprecate old
 Eventually, all Thucydides references will be removed. 
- [40a532d21efa776](https://github.com/serenity-bdd/serenity-core/commit/40a532d21efa776) Updated the Ascii Art banner.
### v1.0.9
** Commits with examples **
- [09927b0fda489ce](https://github.com/serenity-bdd/serenity-core/commit/09927b0fda489ce) Integrated better support for JBehave
- [b3340e5d3756a26](https://github.com/serenity-bdd/serenity-core/commit/b3340e5d3756a26) Integrated better support for JBehave
- [5ea5b718068a34f](https://github.com/serenity-bdd/serenity-core/commit/5ea5b718068a34f) Changed the &#39;checkOutcomes&#39; task to force it to run the tests first.
### v1.0.8
** Commits with examples **
- [e1956cfd278a505](https://github.com/serenity-bdd/serenity-core/commit/e1956cfd278a505) Enable selection of Mac Os version on SauceLabs
- [8344474fc2d7c23](https://github.com/serenity-bdd/serenity-core/commit/8344474fc2d7c23) Added support for the AssumeThat method for JUnit tests - AssumeThat will result in a test being displayed as &#39;ignored&#39; in the reports.
- [40db746819856e7](https://github.com/serenity-bdd/serenity-core/commit/40db746819856e7) Enable selection of Mac Os version on SauceLabs
- [eb4608f6d8c1818](https://github.com/serenity-bdd/serenity-core/commit/eb4608f6d8c1818) Removed some code that used the JDK 8 libraries
- [c12c6ddc076bcb8](https://github.com/serenity-bdd/serenity-core/commit/c12c6ddc076bcb8) Updated to Selenium 2.44.0
- [308ec8f50c5dbcc](https://github.com/serenity-bdd/serenity-core/commit/308ec8f50c5dbcc) Updated the changelog to reflect the serenity-core repo. For Bintray this is a bit of a hack, since the BinTray serenity-core package gets artifacts from two repos, serenity-core and serenity-maven-plugin, which are separate only because of the fact that core needs to be built and deployed before the maven plugin generation task in the serenity-maven-plugin build can be done. So the changelogs will be up-to-date on Github for both repos, but the one on bintray will only reflect core.
- [50c45e31c5432cd](https://github.com/serenity-bdd/serenity-core/commit/50c45e31c5432cd) Adding an automatically generated change log to the build
### v1.0.7
** Commits with examples **
- [00de150f4da3aab](https://github.com/serenity-bdd/serenity-core/commit/00de150f4da3aab) Refactored the gradle plugin
- [66556bb4e71cf65](https://github.com/serenity-bdd/serenity-core/commit/66556bb4e71cf65) Fixed a bug where error messages were incorrectly displayed in the step details
- [6d0f8ee7d7ee3c2](https://github.com/serenity-bdd/serenity-core/commit/6d0f8ee7d7ee3c2) jbehave was pulling in hamcrest 1.1. Excluded hamcrest from the jbehave dependency.
- [4494dee65ac0b1f](https://github.com/serenity-bdd/serenity-core/commit/4494dee65ac0b1f) If javadoc is not told to expect UTF-8 in the strings it uses can generate ASCII errors on at least the Mac.
### v1.0.6
** Commits with examples **
- [2f58c3b419c5330](https://github.com/serenity-bdd/serenity-core/commit/2f58c3b419c5330) Fixed some formatting and navigation issues in the reports
### v1.0.5
** Commits with examples **
- [6780200d8b74535](https://github.com/serenity-bdd/serenity-core/commit/6780200d8b74535) Added the Serenity helper class, as a replacement for the legacy &#39;Thucydides&#39; class
- [08b5502af44c08f](https://github.com/serenity-bdd/serenity-core/commit/08b5502af44c08f) Fixed a bug in the reporting where duplicate story tags were displayed in the screenshot screens.
- [805dbf1a9bf72b6](https://github.com/serenity-bdd/serenity-core/commit/805dbf1a9bf72b6) Logs a message indicating the path of the generated reports after report aggregation.
- [fe1c3c5eb2cee95](https://github.com/serenity-bdd/serenity-core/commit/fe1c3c5eb2cee95) Added the Serenity utility class, which exposes and delegates to methods of the legacy Thucydides class.
- [4138f8900eb6259](https://github.com/serenity-bdd/serenity-core/commit/4138f8900eb6259) Check if a resized file for a given screenshot already exists, and if so don&#39;t perform the resizing
- [0e9d614b462448a](https://github.com/serenity-bdd/serenity-core/commit/0e9d614b462448a) Moved most uses of FileUtils to the Java 7 Files class, in order to remove sporadic issues when resizing screenshots
- [e5a13c7723cb73c](https://github.com/serenity-bdd/serenity-core/commit/e5a13c7723cb73c) SmartAnnotation needs platform for Appium annotations to work
### v1.0.4
** Commits with examples **
- [7a65f64d3bd4d6f](https://github.com/serenity-bdd/serenity-core/commit/7a65f64d3bd4d6f) Fixed a failing test
- [b42d58b33af6ea3](https://github.com/serenity-bdd/serenity-core/commit/b42d58b33af6ea3) Fine-tuning the reports
- [69252742737e848](https://github.com/serenity-bdd/serenity-core/commit/69252742737e848) Support for appium annotations, added accessibility and ui automation for IOS and android
- [52f0eeadcfc82d2](https://github.com/serenity-bdd/serenity-core/commit/52f0eeadcfc82d2) Missed change to PathProcessor
- [e84ac40f8da7831](https://github.com/serenity-bdd/serenity-core/commit/e84ac40f8da7831) Porting changes from thucydides appium-driver-support
- [f07879ca4b94183](https://github.com/serenity-bdd/serenity-core/commit/f07879ca4b94183) Refactored some tests
- [d5511b6706701d4](https://github.com/serenity-bdd/serenity-core/commit/d5511b6706701d4) Cater for rare cases where the driver returns null when an element is not found
- [36d471f7c2acdbd](https://github.com/serenity-bdd/serenity-core/commit/36d471f7c2acdbd) Repositioned the report timestamp
- [80e1ef06258e1e5](https://github.com/serenity-bdd/serenity-core/commit/80e1ef06258e1e5) Repositioned the report timestamp
- [c8fd3b94c1bd867](https://github.com/serenity-bdd/serenity-core/commit/c8fd3b94c1bd867) Added bootstrap tabs
- [4a132ad31b57d7f](https://github.com/serenity-bdd/serenity-core/commit/4a132ad31b57d7f) Added tests to the gradle plugin
- [98073bdbe5ff127](https://github.com/serenity-bdd/serenity-core/commit/98073bdbe5ff127) Added SerenityRunner and SerenityParameterizedRunner classes as alternative names for ThucydidesRunner and ThucydidesParameterizedRunner, more in line with the new naming schema.
- [4c953d868707e2c](https://github.com/serenity-bdd/serenity-core/commit/4c953d868707e2c) Moved the serenity-maven-plugin to a separate project
- [ad4800ebcf39afd](https://github.com/serenity-bdd/serenity-core/commit/ad4800ebcf39afd) Getting the maven plugin build working
- [74df0296738f380](https://github.com/serenity-bdd/serenity-core/commit/74df0296738f380) Fine-tuning the release tagging
### v1.0.2
** Commits with examples **
- [527387e98a503f0](https://github.com/serenity-bdd/serenity-core/commit/527387e98a503f0) Initial release version
- [4a119f5eb78613d](https://github.com/serenity-bdd/serenity-core/commit/4a119f5eb78613d) Added a selector to find buttons by their label, e.g. find(By.buttonText(&#39;Add to cart&#39;));
- [8ba6aeb194a96bb](https://github.com/serenity-bdd/serenity-core/commit/8ba6aeb194a96bb) Honor both &#39;thucydides.properties&#39; and &#39;serenity.properties&#39; files for local project configuration
- [b5732dc3a744246](https://github.com/serenity-bdd/serenity-core/commit/b5732dc3a744246) Let the bintray keys be defined by the build server
- [f2322d488bb19e9](https://github.com/serenity-bdd/serenity-core/commit/f2322d488bb19e9) Minor fix to work around an incompatiblity with IBM JDB 1.7
- [5caf4a28cbcb818](https://github.com/serenity-bdd/serenity-core/commit/5caf4a28cbcb818) Changed group to serenity-bdd to make syncing with Maven Central easier
- [5d3f58a217827dd](https://github.com/serenity-bdd/serenity-core/commit/5d3f58a217827dd) Changed group to serenity-bdd to make syncing with Maven Central easier
- [1d7740dc9d007c0](https://github.com/serenity-bdd/serenity-core/commit/1d7740dc9d007c0) Fixed an issue in the BinTray deployment
- [3620bc2af882c43](https://github.com/serenity-bdd/serenity-core/commit/3620bc2af882c43) Fine-tuning the release pipeline
- [bc0e078f187ae7f](https://github.com/serenity-bdd/serenity-core/commit/bc0e078f187ae7f) Added more info to the README file
- [3049d1465732d6c](https://github.com/serenity-bdd/serenity-core/commit/3049d1465732d6c) Initial move over to Serenity from Thucydides
