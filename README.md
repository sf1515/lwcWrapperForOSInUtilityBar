# DemoContainerOS

This Lightning Web Component (LWC) acts as a wrapper to run OmniScripts from the Salesforce Utility Bar.  
OmniScripts cannot be directly embedded into the Utility Bar, so this wrapper provides the necessary integration.

## Why this component is needed

- Salesforce Utility Bar does not support embedding OmniScripts directly.  
- This wrapper exposes configuration options (Type and SubType) that allow the component to launch a specific OmniScript runtime inside the Utility Bar.  
- It ensures the OmniScript runtime is displayed properly, filling the available panel space.

## How to use

1. Go to **Setup > App Manager**.
2. Select the desired Lightning App and click **Edit**.
3. Navigate to the **Utility Items (Desktop Only)** section.
4. Click **Add Utility Item**.
5. Search for **DemoContainerOS** and add it.
6. In the **Properties** section, provide:
   - **Type**: The OmniScript type.
   - **SubType**: The OmniScript subtype.
7. Save the app configuration.

## Behavior

- Once configured, the component loads the specified OmniScript inside the Utility Bar panel.  
- The OmniScript is rendered using the `omnistudio-omnistudio-standard-runtime-wrapper`.  
- The provided `Type` and `SubType` values are passed into the runtime wrapper to determine which OmniScript to display.
