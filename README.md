# Microsoft CMMC Acceleration Program
This resource is part of the Microsoft Cybersecurity Maturity Model Certification (CMMC) Acceleration Program. Go [here](https://aka.ms/CMMCResponse) to learn more about the program.

# Azure Policy Initiative for CMMC Level 3 (Preview)
This repository contains a sample Azure Policy Initiative for CMMC Level 3.  The policies and controls are derived from those in the NIST SP 800-171, plus additional polices to address the delta between NIST SP 800-171 and CMMC Level 3.  Additional policies will be added to this repository over time.

>DISCLAIMER: _The Policy Initiative for CMMC Level 3 is based upon available information to date and is provided as a sample resource only. Microsoft is not a CMMC accrediting body and thus cannot guarantee any outcome under the formal CMMC review process._

## Prerequisites
1. You should have a basic understanding of [Azure Policy and Policy Initiatives](https://azure.microsoft.com/en-us/services/azure-policy/) before applying this sample. Do not apply this Policy Initiative in any production subscription without first understanding and accepting the potential impact.

2. There are separate policy initiatives for commercial and gov clouds.  When deploying the initiative please select the appropriate file according to your tenant.  For reference the file named 'CMMCL3_Policyinitiative.json' is for commercial deployments only.  The file named 'CMMCL3_Policyinitiaitve_Gov.json' is modified to work in Azure gov. deployments.
  
## Deployment
1. Download this repo and extract to a desired local folder.

2. Run the included PowerShell script **deploy-policySetDef.ps1**. Substitute your own SubscriptionId and path to the definition file.
  ```powershell
  ./deploy-policySetDef.ps1 -definitionFile C:\PolicyInitiatives\CMMC_L3\CMMCL3_PolicyInitiative_Preview.json -subscriptionId 00000000-0000-0000-0000-000000000000
  ```
  **NOTE: The Azure CLI and PowerShell modules refer to a Policy Initiative as a Policy Set.**
  
 ## Next Steps
1. Browse to the Azure Portal and open the **Policy** blade. Verify you see a custom Initiative named **[Preview]: CMMC L3**.

2. You can edit the Policy Initiative to examine and understand what it contains.

3. Browse to the [Azure Blueprint for CMMC Level 3](https://github.com/adamdimopoulos/Blueprints) repo and follow the instructions to import the Blueprint. This will assign the above Policy Initiative for you.

4. Please review all aspects of this Policy Initiative and provide [feedback](https://aka.ms/feedbackazureblueprintcmmc).
  
