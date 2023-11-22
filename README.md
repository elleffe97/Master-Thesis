# Master-Thesis
Methodology to help developers identify smells and decide whether/how to refactor them on a generic microservices system.

## Installation

We will describe the installation process of our project. It could be used on every platform on which the Visual Paradigm application, at least at version 17.0 can run.

You can download Visual Paradigm on the official website: [https://www.visual-paradigm.com/download/](https://www.visual-paradigm.com/download/). Then you need to activate a license to use it and for the aim of the project, the Academical one is enough.

### Editor Plug-in

To execute the scripts you must download and install an editor plug-in. The steps to do it are:

1. Download the project from the GitHub repository [https://github.com/sz332/visual_paradigm_scripting_plugin_oss](https://github.com/sz332/visual_paradigm_scripting_plugin_oss) as a zip file.

2. Install the plug-in in Visual Paradigm following the instructions at [https://www.visual-paradigm.com/support/documents/vpuserguide/124/254/7041_installingpl.html](https://www.visual-paradigm.com/support/documents/vpuserguide/124/254/7041_installingpl.html). We report the simpler one:
   a. In Visual Paradigm, select **Help > Install Plugin** from the application toolbar.
   b. In the **Install Plugin** window, select **Install from a zip of plugin**.
   c. Click **OK**.
   d. Select the zip file in the file chooser and click **Open**.
   e. Restart Visual Paradigm for the plugin to take effect.

### Model Generation

You can skip this section if you run the application on the given Microservice Model of **Online Boutique**.

Otherwise, to use our approach you need to generate a Micro Service Model of your system. As follows the required steps:

1. Open the "**GeneralProject.vpp**" in Visual Paradigm.

2. Right-click on the **Model** folder and in the **Sub Diagrams** windows choose **New Diagram**.
   a. Search for **Composite Structure Diagram**, select it and click on **Next** button.
   b. Select the **Blank** project suggested, then click on **Next** button. Select a name for the diagram and click on **Next** button again.
   c. Construct the model using classes, parts (attributes), and associations. Remember to add the correct stereotypes to all the elements.

### Scripts execution

In this section, we will show how to execute the scripts to obtain the desired results. The instruction will be given in general for every script and in the end, we will give some particular comments about each one of them.

1. Open the project ("**OnlineBoutique.vpp**") in Visual Paradigm and check if all the diagrams are opened by clicking at the bottom on the right side of the workspace. You must see all the 3 diagrams there. If you don't, you just need to double-click on them on the Model Navigator until they open one at a time. Then put yourself on the **Micro Service Model** diagram.

2. Start the just-installed plug-in by clicking on the **Plugin** window and then on the **Script Editor** button. 

3. Copy and paste the content of script "**SIG\_Generator.txt**" and click on the **Execute** button at the bottom left-hand side of the editor window. You should see the just-created SIG behind the window.

4. Drop all the code in the script editor and paste the content of the file "**SS\_Detection.txt**". In this phase, you could interact with the code changing the security smell to be analyzed in the `SecuritySmells` list. Then run the code by clicking on the **Execute** button. The results will be shown on the right-hand side of the Script Editor Windows and you need to save them because they will be the input for the next and last step.

5. Having a list of security smells and their relative affected microservices you can now copy and paste the code from "**SubDiagram\_Generator.txt**" and change the content of the lists `Microservices` and `SecuritySmells` with the just obtained strings. Then execute the scripts and visualize the results in the Model Navigator.
