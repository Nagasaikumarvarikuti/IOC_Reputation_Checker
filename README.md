# IOC_Reputation_Checker

📌 **Introduction to the IOC Reputation Checker Playbook**

The IOC Reputation Checker Playbook is an Azure Logic App designed to automate the investigation of Indicators of Compromise (IOCs)—such as IP addresses, domains, URLs, and file hashes—against external threat intelligence services.

🎯 **Purpose:**

1. Automatically analyze and enrich Sentinel incidents with reputation data.
2. Reduce manual effort for security analysts by fetching IOC intelligence automatically.
3. Improve incident triage and response time in Microsoft Sentinel.

🛠️ **How it Works**

1. Fetches entities from the incident.
2. Iterates through each entity based on its type.
3. Retrieves reputation data from the VirusTotal threat intelligence platform using an HTTP GET request.
4. Updates the incident with the retrieved reputation data.

🏆 **Capabilities**

1. Handles a large number of entities efficiently.
2. Can be used on any type of Sentinel incident.
3. Uses traditional HTTP GET request instead of the VirusTotal Trigger to avoid 429 (quota exceeded) errors when using a general API key.
4. Prints a single comment with all entities in a well-structured tabular format.

🚀 **Deploy Sentinel Playbook**

Click the button below to deploy the **IOC Reputation Check Playbook** to Azure.

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fgithub.com%2FNagasaikumarvarikuti%2FIOC_Reputation_Checker%2Fblob%2FHiday%2Fsanitized_template.json)
