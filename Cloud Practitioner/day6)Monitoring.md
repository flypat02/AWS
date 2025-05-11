# Practitioner Essentials 6일차

## Amazon CloudWatch

- A web service that enables you to monitor and manage various metrics and configure alarm actions based on data from those metrics
- CloudWatch uses metrics to represent the data points for you resuources

## CloudWatch alarms

- With CloudWatch, you can create alarms that automatically perform actions if the value of your metric has gone above or below a predefined threshold

## CloudWatch dashboard

- The CloudWatch dashboard feature enables you to access all the metrics for your resources from a single location

---

## AWS CloudTrail

- Records API calls for your account. The recorded information includes the identity of the API caller, the time of the API call, IP, API caller, and more
- Events are typically updated in CloudTtrail within 15 minutes after an API call

## Example of CloudTrail

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746950400/G-thCgHQZuJu39xB3-PYmQ/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/CPE%20Digital%20-%20Module%207%20-%20AWS%20CloudTrail%20event.png)

## CloudTrail insights

- This optional feature allows CloudTrail to automatically detect unusual API activities in your AWS account

---

## AWS Trusted Advisor

- A web service that inspects your AWS environment and provides real-time recommendations in accordance with AWS best practices
- Trusted Advisor compares its findings to AWS best practices in five categories:
1. Cost Optimized
2. Performance
3. Security
4. Fault Tolerance
5. Service Limits

## AWS Trusted Advisor dashboard

![](https://explore.skillbuilder.aws/files/a/w/aws_prod1_docebosaas_com/1746950400/G-thCgHQZuJu39xB3-PYmQ/tincan/fe470bc5add63f94f005d3da17a6db8131e78b9e/assets/Trusted_Advisor_dashboard.jpg)

- When you access the Trusted Advisor dashboard, you can review completed checks for 5 categories
1. The green check indicates the number of items for which it detected no problems
2. The orange triangle represents the number of recommended investigations
3. The red circle represents the number of recommended actions