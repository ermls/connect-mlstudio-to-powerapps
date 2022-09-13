# connect-mlstudio-to-powerapps
Connect a deep learning model from Azure ML Studio to a Power App GUI

1. Demo Project Description

[Diabetes Predictor Project Description.pdf](https://github.com/ermls/connect-mlstudio-to-powerapps/files/9559216/Diabetes.Predictor.Project.Description.pdf)

2. Demo Data Flow Diagram

[Diabetes Predictor Data Flow Diagram.pdf](https://github.com/ermls/connect-mlstudio-to-powerapps/files/9559222/Diabetes.Predictor.Data.Flow.Diagram.pdf)

3. Deploy a Azure ML Studio Inference pipeline. Note the URI, API Key, and headers which
will be used later.

![1A](https://user-images.githubusercontent.com/83891373/189542792-afe7cf75-be6e-4028-b3ae-5060f1923a0f.jpg)

![1B](https://user-images.githubusercontent.com/83891373/189542797-3d06641a-72a2-480e-8aa5-44f34088c6b9.jpg)

![1C](https://user-images.githubusercontent.com/83891373/189542804-8bdb91df-d0a5-4d02-a87c-78879cef7f79.jpg)

4. Create a Power Automate flow that will be triggered from Canvas Apps. The HTTP step builds endpoint and 
authorization headers, and a JSON from the app inputs to send to ML Studio. The Parse JSON step formats
the output from ML Studio for further processing. The final steps create and format the result from Parse
JSON into a variable that can be processed by control flow steps and sent to the app for display.

![2A](https://user-images.githubusercontent.com/83891373/189542820-16ab2742-084b-4ca5-807e-caaee622f7bb.jpg)

![2B](https://user-images.githubusercontent.com/83891373/189542825-264bed62-6283-4176-a250-b2898baeb79b.jpg)

![2C](https://user-images.githubusercontent.com/83891373/189543363-3535ae7f-f830-4446-b865-8f38b9e651ea.jpg)

![2D](https://user-images.githubusercontent.com/83891373/189542834-8b2ee419-7929-4e59-bf1a-18be3683227f.jpg)

![2E](https://user-images.githubusercontent.com/83891373/189542841-cac25a36-afc2-423d-8cb4-b8c182f10495.jpg)

![2F](https://user-images.githubusercontent.com/83891373/189542844-2da8976e-cd58-4bdd-ad94-f884a9528a7c.jpg)

5. Canvas App built using text input components for the inputs and label components to
display the output. The "Is Patient Diabetic?" button contains code that initializes the Power Automate
flow and sends it the features input by the user. The label component at the bottom contains
code to display the result from Power Automate.

![3A](https://user-images.githubusercontent.com/83891373/189542874-3f4a111a-984b-4008-8407-9a7c3ddeed2a.jpg)

![3B](https://user-images.githubusercontent.com/83891373/189542880-a2e5872d-4fa5-4c24-8e02-3776a72089d3.jpg)

![3C](https://user-images.githubusercontent.com/83891373/189542883-2ca7a56e-bbd4-4197-b0e1-ecb6d0d6f4ef.jpg)

6. Demo of the app in action.

![4A](https://user-images.githubusercontent.com/83891373/189542890-11b4cce9-3258-49c4-a970-219b9519a848.jpg)

![4B](https://user-images.githubusercontent.com/83891373/189542893-d04d9d73-ce3e-4be2-ab03-27b6fb9fa9d5.jpg)
