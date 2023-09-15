# Roadmap
In our technical roadmap, we outline the required minimum to launch Communa as a product and generate revenue through a 5% fee on freelancer income. The platform operates within a framework where freelancers are paid on a weekly basis.

### Here is the workflow:
- Freelancers and clients connect on the website - https://communa.network.
- Clients publish job listings and assign them to freelancers.
- Freelancers select the assigned job on our TimeTracker and log their unconfirmed working hours.
- Clients review and confirm the freelancer's work using our smart contract system.
- Freelancers receive payment after deducting a 5% commission.
- The paid hours are securely stored on the blockchain, contributing to the freelancer's reputation.
- Communa retains a 5% commission from the freelancer's income.

This workflow relies on a website that gives access to job publishing, freelance search, timesheets, and reports; a time tracker desktop app to track automatically time spent while working; and smart contracts for instant payment processing of stable coins like USDT.

## Website
The website facilitates smooth communication between clients and freelancers, allowing clients to post jobs, verify work logs and process payments.

### 💰 Profiles
The profile section is where freelancers can view and edit profile information, including their skills, experience, hourly rate, and availability.
### 💼 Jobs
The platform will provide clients with the ability to effortlessly publish job listings, enabling them to describe the tasks and requirements in detail. Freelancers will be able to apply for jobs by sending an initial message and specifying their desired hourly rate.
### 📝 Reports
Our comprehensive reporting system will automatically track time using our dedicated time-tracking application. The tracked time will be made instantly available for client confirmation, promoting transparency and accuracy. Both freelancers and clients will have access to detailed reports, enabling them to review the tracked time and gain insights into project progress. The system will verify the time logs on the website at the end of each workday or workweek, ensuring reliable and consistent data. The report rendering will be designed to be intuitive and user-friendly, taking inspiration from the effectiveness of Hubstaff.
### 💰 Payments
To simplify and streamline the payment process, freelancers will be required to submit timesheets on a weekly basis, specifying the hours worked for each client. Clients will have the responsibility of reviewing the work logs submitted by freelancers and verifying their accuracy. Once confirmed, clients will be able to submit payments to freelancers based on the agreed-upon rates and the hours worked. The system will ensure secure and efficient payment transactions, fostering trust and satisfaction among users
###  Technical requirements
https://github.com/communa/communa/blob/main/Frontend.md
https://github.com/communa/communa/blob/main/Backend.md


## Time Tracker
Once a freelancer is assigned to a job, a corresponding project becomes available in our desktop application enabling a freelancer to log hours.

### ⏱️ Automatic time tracking
Our time - tracking app will capture various activities such as mouse movements and clicks, ensuring accurate and detailed logs of the freelancer's work. These logs will be sent to the backend every 10 minutes, providing real-time insights into the freelancer's productivity.
### 🖥️ Desktop application
We are developing a dedicated desktop native application for time tracking, providing freelancers with a user-friendly interface to effortlessly track their work hours.
### Technical requirements
https://github.com/communa/communa/blob/main/TimeTracker.md

## Smart Contracts
In the final stage of the process, we facilitate the seamless transfer of crypto payments for the tracked hours with our smart contract and increase the reputation of a freelancer.

### 👛 MultiSig wallet
For deployment and development purposes we rely on multisig wallets giving us enhanced security and allowing for efficient management of funds.
### 🔖 Payments and reputation
Facilitate the needed functionality for payment processing and reputation, leading to a seamless experience with payments released to freelancers in USDT(a stablecoin) on a weekly basis.
