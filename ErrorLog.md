Error build failed 2/22/222
- Running a Spring Boot Project BUILD FAILURE, test failures
    - look in surefire-reports for indiviual test results
    `Failed to create query for method public abstract java.util.Optional com.revature.data.CustomerRepository.findByUsername(java.lang.String)! No property username found for type Customer! Did you mean 'userName'?`
    - Solution: method name in @Reposiotry `findByUserName(String userName)` was
        `findByUsername(String userName)`
         