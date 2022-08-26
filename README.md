# CI-CD-Pipeline
This is a demo project created to create a CI/CD pipeline using Jenkins


Creating a job for each section (Build > Deploy > Test > Release)

- Created a free style project for Deply 

![image](https://user-images.githubusercontent.com/59870615/186907839-4c8fa282-f8c3-4df3-83fe-008edcc111d1.png)
- Adding a script to echo succesful message
![image](https://user-images.githubusercontent.com/59870615/186908246-fee4379b-9529-451b-851c-40cb56eeb3d7.png)

- All the jobs are created and formation of chain is important

![image](https://user-images.githubusercontent.com/59870615/186908778-0f0c8906-6cd4-4347-88df-a0b74a23ede1.png)


Creating a chain between the jobs and adding upstream and downstream jobs
(Build -> Deploy -> Test -> Release)

- Upstream jobs: The job which will run before the current job is upstream job 
- Downstream jobs: The job which is run after the succesful execution of this job
(ex. **Build** is upstrem job - **Deploy**  - downstream job is **Test**)

- Now move configure > Build Target of (**SampleDeployJob**)
![image](https://user-images.githubusercontent.com/59870615/186911304-3ef90bbc-bd59-477a-af34-527713a53a4d.png)
![image](https://user-images.githubusercontent.com/59870615/186911474-6a5a3e67-7d3d-440f-90be-818b17c2e4b9.png)
- Now select ```Trigger only if build is stable``` option and make SampleBuildJob as upstream.
- Repeat the same step for the Test, Release jobs also. 
