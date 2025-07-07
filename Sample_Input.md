# Sample Input & Output Data (Unstructured → Structured Transformation)

This sample demonstrates how unstructured ticket content was automatically processed using AI Prompts in Power Automate (AI Hub) and Copilot Studio, resulting in structured data stored in SharePoint.

---

## 🎯 Sample Unstructured Input (Email Body Example)

Harry Potter, identified by Applicant ID 14560, holds the position of Innovation Engineer within the Data Engineering & Analytics department. They report to their designated line manager and are classified as a permanent employee with an annual salary of 100,000.
Their employment began on 05/02/2024. The applicant's office is located at [Office Address], and they can be contacted via phone at [Phone Number]. Based in [Country] and operating from the [Region] region, their system credentials have been created with a designated username and password, along with an assigned User Principal Name for company systems.
Additionally, the applicant is associated with a specified external supplier and has been assigned to various system groups, including but not limited to:
Standard AD Groups
Microsoft 365 Group
Expense Management Platform
Helpdesk System
HR Management System
Security Awareness Platform
Space Booking System
Azure Directory Groups
The applicant has also been set up for graphical email signatures and enrolled in conditional access policies for device and application security.
Furthermore, the applicant's profile includes US-specific attributes and additional company updates, based on organizational requirements.

---

## ✅ Structured Output (SharePoint List Format)

| Field                                    | Value                       |
|------------------------------------------|-----------------------------|
| Applicant ID                             | 14560                       |
| Applicant Name                           | [Applicant Name]            |
| Job Title                                | Innovation Engineer         |
| Line Manager                             | [Line Manager Name]         |
| Department                               | Data Engineering & Analytics|
| Salary                                   | 100000                      |
| Type of Employment                       | Permanent                   |
| Date of Joining                          | 05/02/2024                  |
| Address                                  | [Office Address]            |
| Phone Number                             | [Phone Number]              |
| Country                                  | [Country]                   |
| Region                                   | [Region]                    |
| System Username                          | [Username]                  |
| System Password                          | [Password]                  |
| User Principal Name                      | [User Principal Name]       |
| Supplier Name                            | [Supplier Name]             |
| Standard AD Groups                       | ADGroup-12345               |
| Microsoft 365 Group                      | M365Group-67890             |
| Expense Management Platform              | ExpenseGroup-23456          |
| Helpdesk System                          | HelpdeskGroup-34567         |
| HR Management System                     | HRGroup-45678               |
| Security Awareness Platform              | SecurityGroup-56789         |
| Space Booking System                     | BookingGroup-67890          |
| Azure Directory Groups                   | AzureGroup-78901            |
| Enable Graphical Signature               | Yes                         |
| Conditional Access Policies Enforced     | Yes                         |
| US Specific Attributes                   | Yes                         |
| Company Updates Subscription             | Yes                         |

---

**Note:**
- Names, addresses, phone numbers, and group IDs are anonymized for demonstration purposes.
- This data reflects the structured SharePoint list fields that are automatically populated by the process.

---

**Note:** Group IDs are anonymized with placeholder names for demonstration.

---

## 🔍 Explanation:
- **Input:** Unstructured, natural-language email text from HR.
- **Output:** Structured data ready for automation in SharePoint & Power Automate.
- This transformation is performed by an AI-based prompt and Power Automate flow integrated with Copilot Studio.

