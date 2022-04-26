# Handy Configuration File And Hints
Handy tips and hints on how to handle crazy configuration on one machine.<br><br>
Hi, I'm Woja. 
I work and study at the same time and I have been doing so since 2 years. 
As a student, I study Computer Science at PUT, as an employee I am a Software Engineer. 
Due to the fact that commuting between office and university is my daily workout, 
I prefer to take just one laptop instead of two.
So... I need to solve my problems with configurations on a daily basis to have all 
my setups on one mashine.<br>
I want to share my flow, maybe someone on this planet has the same problems.
## git config for two separete accounts
So I have two Github accounts and I want to use both of them smoothly. This is
the way which lets me achieve that.
### Prerequisites
Example user data for work account
```
name = Example Name
email = example_name@workmail.com
```
Example user data for personal account
```
name = Example Name
email = example_12345@randommail.com
```
### ssh keys generation
For every Github account a pair of private/public ssh keys is needed.<br>
Generate a pair of private/public ssh key for your work account:
```
ssh-keygen -t rsa -C "example_name@workmail.com"
```
When ask for file set name:
```
Enter file in which to save the key (~/.ssh/id_rsa): ~/.ssh/id_rsa_work
```
Generate a pair of priavte.public ssh key for your personal account:
```
ssh-keygen -t rsa -C "example_12345@randommail.com"
```
When ask for file set name:
```
Enter file in which to save the key (~/.ssh/id_rsa): ~/.ssh/id_rsa_personal
```
Add ssh keys as following:
```bash
ssh-add ~/.ssh/id_rsa_work
ssh-add ~/.ssh/id_rsa_personal
```
