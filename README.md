Cloud Engineer Offline Exam

Preview:

![image](https://user-images.githubusercontent.com/48853390/186352839-638e069c-8f32-4e5b-8c23-b69487af88be.png) 

Filename: Untitled Diagram.drawio


Output is incomplete and below is the Q&A.

Part 1
- Create a system infrastructure draft using AWS services and middleware using diagrams and text.
  All resources I used was AWS resources and not familiar with middlewares outside AWS, except for Github/Innersource/Azure Repo.
- Consider applying CI / CD and ensuring scalability and availability.
  This was not added in the diagram but could be implemented using any of Git Repositories(GitHub, Innersource, Azure Repo).
  Upon commit on target repo, AWS CodePipeline will catch the event and trigger CodeBuild.
  Depending on the repo it will put the result to S3[FE] or ECR[BE] 
  For FE after build, and assets are uploaded to target S3 bucket, it will then trigger invalidation in CF.
  For BE after build, I am not familiar how ECS work after build package was pushed in ECR.
- Please explain in a sentence why you chose such a configuration.
  - CloudFront
    Have actual experience using CloudFront with Azure Pipeline.
  - API Gateway
    Have actual experience using API Gateway but by only invoking Lambda resources. Not familiar how it will work with docker containers and my assumtion is it will handle the concurrency in container cluster level.
  - Amazon RDS for MySQL
    Data relation is quite simple.
  - EC2 Container Service
    No acutal experience and not very familiar on how container service work. Only have experience debugging kubernetes Pods using kubectl.
  - SNS
    Familiar on how it is used for sending email.
- What additional questions should you ask PO in the future to design better? If you have, please describe it.
  - How many environments to be created?
  - Create Geolocation routing policy?

Part 2
- Can you please explain in detail the work experience over the last three years. What kind of technology, what kind of solution, what kind of difficulties did you face? What was the work procedure you did?
  For the last three years my work was mostly Backend and a little of Frontent changes. As a backend developer, I am mostly given a User Story and implement the feature based on the requirements. Solutions are already provided. My work, atleast for me are all straight forward and difficulties happen when the initial solution is not applicable/lacking, but those issues are mostly resolved by Technical Architect/Lead. For the past three years, I have little to none experience with regards to DevOps tasks.
- Write an Ansible recipe that builds an environment of nginx, mysql, laravel into an instance of ec2 that can withstand the production environment.
  No prior knowledge.
- Create a docker image, DockerFile and DockerCompose file when the environment created above be dockerized.
  No prior knowledge.
