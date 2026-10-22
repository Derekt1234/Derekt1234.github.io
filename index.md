---
layout: default
title: Professional Self-Assessment
---

## Professional Self‑Assessment

Completing the Computer Science program at Southern New Hampshire University and developing this ePortfolio has given me the opportunity to reflect on my growth as a developer and the strengths I bring to the field. Throughout the program, I learned how to approach problems with a structured engineering mindset, communicate clearly with both technical and non-technical stakeholders, and collaborate effectively in team environments. These experiences helped shape my professional goals and prepared me to enter the industry as a full-stack developer with a strong foundation in secure, reliable software design. 
  
Across my coursework, I gained hands-on experience with data structures, algorithms, software engineering principles, databases, and security. Courses such as CS-300 Data Structures and Algorithms strengthened my understanding of algorithmic thinking and performance trade-offs. While CS-465 Full Stack Development I and DAD-220 Database Systems/Environment helped me build and refine full-stack applications using Node.js, Express, MongoDB, and modern development practices. Security-focused courses taught me the importance of validation, sanitization, and defensive coding, which were skills I carried into my capstone enhancements. 

Developing this ePortfolio allowed me to bring all of those experiences together. Each artifact highlights a different part of my skill set: 

  - Automated testing and CI workflows demonstrate my commitment to quality and maintainability.
    
  - Pagination and sorting logic showcase my ability to apply algorithmic reasoning to real applications.
    
  - Improving database validation reflects my focus on secure, predictable backend design.
    
Together, these enhancements show that I can analyze an existing system, identify where improvements can be made, and implement solutions that follow industry standards. 

This portfolio represents my abilities as a developer and serves as a strong introduction to the work I can produce. It shows not only what I have learned in the program, but also how I have grown professionally, technically, and personally. As I move into the field of computer science, I am confident in my ability to be able to contribute to a development team, communicate effectively, and continue building secure software.  


### Collaboration and Communication
Across the program, I learned how to work effectively in collaborative environments, communicate technical decisions clearly, and document code in a way that supports team understanding. My code review video demonstrates my ability to walk through a codebase, identify weaknesses, and communicate planned enhancements to a technical audience.

### Software Engineering and Design
I gained experience in full‑stack development, modular design, debugging, and structured development lifecycles. My Software Engineering enhancement adds automated testing and a CI/CD workflow, demonstrating industry‑standard engineering practices that improve reliability and maintainability.

### Algorithms and Data Structures
I strengthened my ability to design efficient solutions using algorithmic principles. In my Algorithms & Data Structures enhancement, I implemented pagination and sorting logic using skip/limit calculations and ordering algorithms. This improved performance and demonstrated my ability to evaluate trade‑offs in computing solutions.

### Databases and Security
I developed a security mindset by implementing validation, sanitization, and schema constraints to protect data integrity. My Database enhancement ensures that only clean, safe, and properly formatted data enters the MongoDB database, aligning with secure coding principles.

### How My Artifacts Fit Together

The three enhanced artifacts in this portfolio come from my Travlr MEAN stack application. Each enhancement focuses on a different core area of computer science:

- **Software Engineering:** Automated testing + CI/CD  
- **Algorithms & Data Structures:** Pagination + sorting  
- **Databases:** Validation + sanitization

Together, these enhancements demonstrate full‑stack development skills, algorithmic reasoning, secure backend practices, and professional engineering workflows. They form a cohesive representation of my abilities as a future full‑stack engineer and reflect the program outcomes of the CS degree.

## Code Review Video
The code review video presents the artifacts within my Travlr application and the enhancements to be performed.

[Code Review - Travlr Application](https://youtu.be/KXu_o2-XuBM)

## Original Artifact

The artifact that I chose to perform all three enhancements with is my full-stack MEAN Travlr application from my CS-465 Full Stack Development I course.

[Click here to view original artifact]()

## Enhancement One: Software Engineering and Design

For this enhancement, I focused on improving its backend testing and adding continuous integration. The project now includes Jest unit tests for the trip model and controller, a SuperTest integration test for the trips API, npm scripts for running tests, and a GitHub Actions workflow that runs the API tests on pushes and pull requests. 

I included this artifact because it gives me a practical way to be able to demonstrate how I approach software quality. The tests show that I can check behavior at different levels. The model test verifies the data, the controller test isolates trip creation by mocking the database save, and the API test sends a request through the Express application and verifies the response. The workflow adds an automated check to the development process. 

I made progress toward all five outcomes. For Outcome 1, the GitHub Actions workflow supports collaboration by giving contributors a consistent test result on pushes and pull requests. Outcome 2 is supported by structured testing and clear comments throughout the additions. Adding Jest, Supertest, and automated CI applies established industry tools to improve software quality, which supports Outcome 4. As far as updates for the outcome-coverage plans, Outcome 3 and Outcome 5 did not work out as expected. Outcome 3 was only partially demonstrated because it mostly checks basic data fields, a mocked saved response, and whether the API returns an array. It doesn’t show much algorithmic design or evaluation. Outcome 5 ended up being the weakest due to the fact that reliability checks aren’t the same as security testing, and the current tests don’t probe authentication or authorization. Those outcomes will need to be planned in the other two enhancements. 

This enhancement process taught me that tests are useful not only for catching defects, but also for revealing assumptions about how application parts depend on each other. I had to distinguish a unit test from an integration test, isolate controller behavior with mocks, and make sure the API test handled the Express app correctly. I also encountered issues involving relative module paths and resources that remained open after the tests finished. Resolving the Jest open handle warning helped me understand that test cleanup matters. A test can pass the assertions and still leave a database connection or process running. I had to move the MongoDB startup out of app imports and into the server entry point.  Another problem I encountered was separating the Angular tests from the Jest tests. The Angular tests were basic creation testing templates, but I did not want to delete the files. Overall, I learned to consider testability and cleanup as part of designing and maintaining the application. I also learned that it is much more difficult to add tools after development.


[Travlr Repository](https://github.com/Derekt1234/cs465_fullstack)

## Enhancement Two: Algorithms and Data Structures

For this enhancement, I added server-side pagination and sorting to the trip listing API and integrated the new logic into both the Angular admin interface and the public travel page. 

I selected this artifact because it provides a clear, practical way to demonstrate algorithmic thinking within a real full-stack application. Pagination and sorting are widely used, and implementing them required me to apply algorithmic principles directly to a real backend system. 
Several components of the enhancement showcase my skills in algorithms and data structures. There is Pagination logic where I implemented skip/limit calculations to determine which subset of trips should be returned for the given page. The Sorting logic was applied so the API now sorts trips by code. The paginated API response structure that the enhanced endpoint returns includes page, pageSize, total, and totalPages, which shows my ability to design structured data responses. Then, the integration with both front ends, where the Angular admin interface and the public travel page now request specific pages, as well as display pagination controls. This shows my ability to apply algorithmic improvements across multiple layers of the full stack application. 

I planned for this enhancement to address outcomes 2, 3, 4, and 5. After completing the enhancement, I can say that I met these outcomes. The pagination and sorting logic required algorithmic design, validation, and structured communication through both the code and documentation. The enhancement also improved reliability by ensuring that the API returns predictable data rather than large unstructured arrays. 
	
Enhancing the artifact taught me several important lessons about algorithmic design in real applications. First, I learned how important it is to think about scalability early. Even though the Travlr app originally had only a few trips, implementing pagination made me consider how the system would behave with dozens of records. Designing the skip/limit logic helped reinforce how a small algorithmic design can have large impacts on performance. Second, integrating pagination into both the admin Angular interface and the public travel page taught me how algorithmic improvements move through the entire system. Updating the API was only the first part. I also had to update the UI logic, handle empty states, and ensure that page boundaries were correct. This helped me better understand how frontend and backend systems can coordinate around algorithmic behavior. 
The biggest challenge I faced was ensuring that pagination behaved properly under all conditions. I felt like every time I would update one part of the application, then 2 parts would go down. It became a game of cat and mouse, and testing these scenarios strengthened my debugging skills. 



[Travlr Repository](https://github.com/Derekt1234/cs465_fullstack)

## Enhancement Three: Databases

For this enhancement, I enhanced the database layer of my Travlr application artifact, specifically the API logic that handles creating and updating trip data. This includes the Mongoose schema, the POST and PUT controllers, and the new validation and sanitization middleware. The original artifact was created in my CS-465 Full Stack Development I course, but I have now used this artifact for all three enhancements and have improved security, reliability, and data integrity. 

I selected the artifact because it demonstrates my ability to design secure, reliable backend systems and work directly with databases. The enhancement shows schema design, API development, input validation, sanitization, error handling, and secure coding practices. I improved the artifact by adding strict schema constraints, implementing validation middleware, adding sanitization to prevent injection attacks, and updating the controllers to use consistent REST responses and proper error handling. 

This enhancement did meet the outcomes I planned to address. It demonstrates my ability to use professional tools and techniques in software engineering and database design, and it shows a security mindset by anticipating malicious input and preventing unsafe data from entering the system. 

Enhancing this artifact taught me how important it is to validate and sanitize user input at multiple layers of the application. I learned how schema constraints, middleware, and controller logic work together to create a secure and predictable backend. One challenge was ensuring that validation, sanitization, and schema rules did not conflict with each other, especially when handling user input text fields. Another challenge was updating the controllers to return consistent and meaningful error messages. I also had to update a few tests with the change in logic. Overall, the process helped strengthen my understanding of secure backend development and improve the reliability and security of the application. 


[Travlr Repository](https://github.com/Derekt1234/cs465_fullstack)
