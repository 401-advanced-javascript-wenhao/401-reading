# Reading 4 - Advanced MongoDB/Mongoose - 4/16/2020

* In Memory Database Testing
  * Pros:
    * No mocks needed
    * Faster development cycle
    * Testing the code that will be in production, not an old/incorrect/incomplete mock
    * Esay to write the test
  * Cons:
    * Needs to seed the database
    * Needs more memory
    * Tests take longer time to run

* Setup & Install dependencies
  * `npm install --save mongoose`
  * `npm install --save-dev jest mongodb-memory-server`
