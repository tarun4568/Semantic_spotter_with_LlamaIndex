# Project Name
**Symantic Spotter using LlamaIndex.**

> Prerequisite to run the Symantic Spotter.

**Step1. :** Run all the cell in install all required library and depended code.


- How to Run the Symatic Spotter:

Run the cell to read all the pdf files by SimpleDirectoryReader.

Once the data loading is done there are two ways to execute the query over list of insuracne documents. 

**1. For sinle Query:** you can directly pass the query to query method of query_engine object or to the query_response method. 
- Sample Query and Resposne:

- Q: print(query("when a person can receive the claims?").response)

- Respone: 

'A person can receive the claims after submitting all necessary claim documents within 60 days from the date of diagnosis of the condition. However, the insurance company may consider condoning the delay in claim intimation if valid reasons are provided for the delay.
Check further at Copy of HDFC-Life-Easy-Health-101N110V03-Policy-Bond-Single-Pay.pdf Page No 13
Similarity score is :0.8287403603706133'

**2. Using testing_pipeline method for multiple questions: **
Create a list of test questions and passed to testing_pipeline. it will ask for feedback please reposnd with good or bad. 

- Sample Query and Resposne:
- Q:
- questions = ['What is beneficiary in HDFC insurance policy',
             'Which is company name is talking about in provided context?',
             'Who is eligible member in the context of insurance policy?',
             'When a person can recieve the claims?']
             
> testing_pipeline(questions):   

> Response from Semantic Spotter:


- What is beneficiary in HDFC insurance policy
The beneficiary in HDFC insurance policy is the individual or entity designated by the insured member to receive the benefits under the policy in the event of the insured member's death. The beneficiary can be a nominee chosen by the insured member and filed with the policyholder. If no nominee is designated or if the nominee predeceases the insured member, the benefits will be payable to the legal heir of the insured member.
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf Page No 11
Similarity score is :0.8504116368845972


Please provide your feedback on the response provided by bot
good

- Which is company name is talking about in provided context?
HDFC Life
Check further at Copy of HDFC-Life-Group-Poorna-Suraksha-101N137V02-Policy-Document.pdf Page No 18
Similarity score is :0.757921216090719


Please provide your feedback on the response provided by bot
good
Who is eligible member in the context of insurance policy?
An eligible member in the context of the insurance policy is a person who satisfies the mentioned Eligibility Criteria and is aged less than the Benefit Expiry Age.
Check further at Copy of HDFC-Life-Group-Term-Life-Policy.pdf Page No 15
Similarity score is :0.8787312173092846


Please provide your feedback on the response provided by bot
good

- When a person can recieve the claims?
A person can receive the claims under the Policy after submitting all necessary claim documents within 60 days from the date of diagnosis of the condition. However, the delay in claim intimation may be condoned if valid reasons are provided for the delay.
Check further at Copy of HDFC-Life-Easy-Health-101N110V03-Policy-Bond-Single-Pay.pdf Page No 13
Similarity score is :0.8206031103341381


Please provide your feedback on the response provided by bot
good

	Question	Response	Page	Good/Bad
0	What is beneficiary in HDFC insurance policy	The beneficiary in HDFC insurance policy is th...	:0.8504116368845972	good
1	Which is company name is talking about in prov...	HDFC Life<br> Check further at Copy of HDFC-Li...	:0.757921216090719	good
2	Who is eligible member in the context of insur...	An eligible member in the context of the insur...	:0.8787312173092846	good
3	When a person can recieve the claims?	A person can receive the claims after submitti...	:0.8206031103341381	good








