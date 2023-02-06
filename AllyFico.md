** ***1. Can you explain your understanding of DevOps and how it differs from traditional software development methodologies?***
   
  ## Traditional SDLC
    - Waterfall approach (earliest and mostly utilized)
    - Separate departments that were individually responsible for developing, testing and delivering
    - Each phase must be completed before the next one can begin - noo overlap
    - It advances in a systematic downward manner

   -   merge conflicts were higher. 
   -   post-production flaws.
    
## DevOps software development

    - DevOps puts emphasizes on collaboration and communication between development and operations teams in order to 
    - It's practice includes continuous integration and continuous deployment. This ensures you always have a ready-to-deploy build.
    - It's an endless cycle consisting of the following steps: plan, code, build and test, release, deploy, operate, monitor, give feedback, and finally reset the loop.
    - All code changes are automatically merged, tested and deployed to a suitable production environment.

    

***2. How do you use tools such as Git, Jenkins, and Ansible to automate the software development and deployment process?***

    - Git, Jenkins, and Ansible are automation tools that help in much of the software development and deployment process, from building and testing code changes
    
    - Git: A version control system 

    - Jenkins: Jenkins is a continuous integration and continuous delivery (CI/CD) (It can be integrated with Git)

    - Ansible: Ansible is a configuration management tool that automates the deployment and management of software.

***3. Can you walk me through a recent project you managed using DevOps practices and the challenges you faced?***

   So, there is this project I developed that will help my mother manage her garden produces. This is a react web application.

    - After the ideation and documenting user stories, I used JIRA, Scrum template per say to have sprints and broke down large stories into bite-sized pieces of value.

   - Git repository to manage the source code and Jenkins to automate the build process. Whenever code changes were pushed to the repository, Jenkins automatically built and tested the application.
   - Had SonarQube integrated with Jenkins to help improve code quality

   - Despite challenges I faced with the new technologies like Jenkins and SonarQube, I completed the project was successfully:
   

***4. How do you use containerization and orchestration technologies, such as Docker and Kubernetes, to improve scalability and reliability?***

    Containerization is the process of packaging an application with the OS, libraries, configuration files, and dependencies it needs into a lightweight bundle of software.

![Alt text](https://miro.medium.com/max/4800/0%2AvluSh-2PnE8IjxD6.webp)

    - With Dockerfile, Docker allows developers to easily build images —   which are essentially templates for creating containers 

    - So how does Kubernetes help when containers fail or when traffic spikes?

    -  Kubernetes is self-healing: when a container goes down, Kubernetes will replace that container. It will also kill off any containers that don’t pass user-defined health checks.

    - Kubernetes also has automated rollouts, rollbacks, and load balancing. This way, network traffic can be distributed across many containers, and new containers are launched and terminated as needed.


***5. Can you explain how you use monitoring and logging tools, such as Prometheus and ELK, to improve visibility and troubleshoot issues in a production environment?***

    Together, Prometheus and ELK can provide comprehensive visibility into the performance and behavior of applications and infrastructure, helping organizations to:

    Proactively monitor performance:

    Troubleshoot issues more efficiently: 

    Improve collaboration and communication: 

    Enhance security and compliance: 

    Prometheus is a monitoring and alerting tool that collects and stores time-series data, such as resource utilization, application performance metrics, and system logs. This data can be used to visualize and analyze performance, identify trends, and set up alerts to proactively detect and address issues.

    ELK (Elasticsearch, Logstash, and Kibana) is a log analysis platform that collects, parses, and stores log data, and provides an intuitive user interface for searching, analyzing, and visualizing logs. ELK can help quickly identify and resolve issues by providing a centralized view of all log data, making it easier to find the root cause of problems.

    

***6. How do you handle and manage infrastructure as code using tools such as Terraform or CloudFormation?***

    - With Infrastructure as Code (IaC), configuration files are created that contain your infrastructure specifications, which makes it easier to edit and distribute configurations. It also ensures that you provision the same environment every time. By codifying and documenting your configuration specifications, IaC aids configuration management and helps you to avoid undocumented, ad-hoc configuration changes.

    - CloudFormation is an IaC tool provided by Amazon Web Services (AWS) that allows organizations to model and set up their AWS infrastructure using a JSON or YAML template. CloudFormation provides a centralized way to manage AWS resources, making it easier to automate, track changes, and revert to previous configurations if necessary.


***7. Can you discuss your experience with continuous integration and delivery (CI/CD) pipelines?***
    
    - Continuous integration establishes an automated way to build, package, and test their applications

    - Continuous delivery picks up where continuous integration ends
  
    - Continuous delivery is the automation that pushes applications to one or more delivery environments. Development teams typically have several environments to stage application changes for testing and review. A devops engineer uses a CI/CD tool such as Jenkins, CircleCI, AWS CodeBuild etc
  
    - Jenkins users define their pipelines in a Jenkinsfile that describes different stages such as build, test, and deploy.

  

***8. How do you use tools such as JIRA or Trello to manage and track work in a DevOps environment?***

    - They are use to help organize project workflows, assigning tasks to team-members and track individual team member work and the entire project work progress more effectively. 
  
    - Collaboration and communication, and enhance visibility and transparency, ultimately helping teams to deliver high-quality software faster and more efficiently.
  
    - Helps in decision making

***9. Can you explain how you use A/B testing and canary releases to minimize risk and improve the release process?***

    - A/B testing and canary releases are two techniques that can be used to minimize risk and improve the release process.

    - A/B testing is a method of comparing two or more variations of a product or feature to determine which one performs better. 

    Canary releases, on the other hand, is a technique for releasing code changes to a small subset of users before rolling them out to a larger audience.


***10.How do you foster a culture of collaboration, automation, and continuous improvement within a DevOps team?***

    - DevOps team requires a focus on creating a supportive and inclusive environment that encourages and rewards collaboration, innovation, and learning.

    - Encourage collaboration: Having coffee time chat centered around your successes and shortfalls, JIRA, GitHub, slack,  etc

    - Embrace automation: Automation is a  way of reducing manual processes by automating repetitive tasks. We use tools like SonarQube, Jenkins etc

    - Encourage continuous improvement: Teams should continuously evaluate their processes and identify areas for improvement. 

    - Foster a culture of learning: Teams having periodical skill levelup meetings or seminars

    - Lead by example: Leaders should model work practice or environment that add values 








**