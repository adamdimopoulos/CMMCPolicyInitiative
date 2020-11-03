# PolicyInitiatives
This repository contains the sample Policy Initiative for CMMC Level 3.  The underlying policies and controls are derived from those in the NIST 800-171 initiative, plus a few extra polices to address a subset the 20 controls, which are the delta between 800-171 and CMMC Level 3.  Additional policies for both frameworks will be added to this repository over time and prior to releasing in preview later this year.

# Prerequisites
This doc assumes you have a basic understanding of how Azure Policy and Policy Initiatives work. 
  
# Deployment
1. Download this repo and extract to a desired local folder.

2. Execute the included powershell script "deploy-policySetDef.ps1", substituting your own subscriptionid and path to the definition file: 
  ```powershell
  ./deploy-policySetDef.ps1 -definitionFile C:\PolicyInitiatives\CMMC_L3\CMMCL3_Policyinitiative.json -subscriptionId 00000000-0000-0000-0000-000000000000
  ```
  
  **In Azure CLI and Powershell modules, a Policy Initiative is referred to as a Policy Set.  Also the github workflow and policies folders can be ignored for the sake of evaluating this sample**
  
  # Next Steps
  
Go to the Azure portal > Policy blade to verify you see a custom initiative named [Preview]: CMMC L3.  You can edit or assign the policy initiative directly from the portal to begin evaluation.  Or proceed to the [Blueprints](https://github.com/adamdimopoulos/Blueprints) repo and follow the instructions to import the CMMC L3 Blueprint into your subscription, which will assign the policy initiative for you.  Please provide applicable [feedback](https://aka.ms/feedbackazureblueprintcmmc) using the link provided in either repo.

  
