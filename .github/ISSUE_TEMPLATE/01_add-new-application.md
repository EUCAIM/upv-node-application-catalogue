---
name: "📦 Request for addition of a new application"
about: "Do you want your application to be added in the catalogue?"
title: 'Add application: <your application name>'
labels: 'add-application'
assignees: ''

---

<!-- Please replace the example content for each section and remove the comments like this. -->

# my-application  <!-- replace here with your application image name, please use only lowercase letters, numbers and hyphens -->

## Description
<!-- Replace here with a description of the application, the features included... -->
This is a tool to do something with a dataset...

## Usage
<!-- Modify this example putting the name of your application and the parameters accepted, 
     those which the user can put after the "--" in the `jobman submit` command 
     (they will be appended to the `ENTRYPOINT` of your image). 
     The input and output directories are the most common, but you can change or add any other. -->

`jobman submit -i my-application -- <INPUT_DIR> <OUTPUT_DIR>`
  
The application accepts 2 parameters:
 - The input path of a DICOM directory
 - The output directory where harmonized image will be saved.
 
Example:  
  ```
    jobman submit -i my-application -- ~/datasets/87f3be56-4725-45c3-9baa-d338de530f73/ ~/persistent-home/results/
  ```
Note the output directory path should be any within the persistent-home, which is shared between all desktops and jobs created by the user, 
otherwise the results will be lost after the end of the job.

<!-- It is recommended to add a usage example, as you can see. 
     For that usage examples take into account that...
      - In the arguments where the user set the path for **image inputs** you should use the path of a dataset (`/home/ds/datasets/<dataset-id>` or just `~/datasets/<dataset-id>`).  
      - In the arguments where the user set the path for **output results**, you should use a directory within the persistent home (`/home/ds/persistent-home/results`or just `~/persistent-home/results`).  
-->

## Authors
James Gordon   <!-- You can put here your name, nick and/or your organization -->
grycap.upv.es

## Contact info
<!-- Replace this example with an email address or publicly accessible contact form to allow the user report issues or request missing documentation required for usage. -->
james@email.com
https://github.com/EUCAIM/upv-node-workstation-images/issues

## URL
<!-- Replace this example with the link to the public or private repository where you put the Dockerfile and all the dependecies available for us to build the image. -->
Public dockerfile repository:
https://github.com/EUCAIM/upv-node-workstation-images/tree/main/ubuntu-python

## License
<!-- Replace here with the URL to the license document of your application.
     Usually it's a file in the code repository URL indicated in the previous section. 
     If there is not any license just put "None".  -->
https://github.com/EUCAIM/upv-node-workstation-images/blob/87a57cff6b79d8c85dc65a3f01a27e3f967d22a4/LICENSE

<!-- If it is a file in private repository, it will be copied (only that file) to the Application Catalogue to make it accesible to the users. -->

