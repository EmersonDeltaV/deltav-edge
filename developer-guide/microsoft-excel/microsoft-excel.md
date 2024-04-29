# How to use Edge Environment in Microsoft Excel

Here are step-by-step instructions for setting up your environment and configuring the necessary components to work with the Rest API Certificate and Bearer Token.

1. **Download and Install the Rest API Certificate**:
   
    - If you already have the certificate, simply download it and proceed to install the DER Certificate.
    - In case the certificate is not available:
      
        1. Access your Edge Manager portal: Edge Manager
        2. Navigate to the "Certificates" section.  
        <img src="images/edge-admin-certificates.png" width=300><p>
        3. Generate the Rest API Certificate.  
        <img src="images/rest-api-certificate.png" width=300><p>
        4. Download the certificate.
        5. Install it on your system.  
        <img src="images/install-rest-api-cert.png" width=300><p>


3. **Configure Microsoft Excel for Rest API Access**:
    - Open Microsoft Excel.  
    - Go to **Home > Data > From Web**.  
    <img src="images/ms-excel-get-data.png" width=300><p>
    - A form will appear.  
    <img src="images/ms-excel-from-web.png" width=300><p>
    - Fill in the "URL Parts" with the appropriate details (e.g., `https://{edge ip}/edge/api/v1/ae`).

4. **Set HTTP Request Header Parameters**:
    - Add an HTTP request header parameter:
        - Name: `Authorization`
        - Value: `"bearer {bearer_token*}"`

5. **Obtain the Bearer Token**:
    - Query the following URL: `https://{edge ip}/edge/api/v1/Login/GetAuthToken/profile`.
    - Provide the necessary body parameters (Username and Password) to authenticate and retrieve the bearer token.

4. **Copy access token from the result and paste it in the Microsoft Excel form**:  
    <img src="images/bearer-token-sample.png" width=800><p>
    
Remember to replace `{edge ip}` with the actual IP address of your Edge server. These instructions will guide you in effectively using the Rest API and Bearer Token within Microsoft Excel. 🚀

And thats it! You can now Retrieve your data to the PowerBI and Create Reports, Dashboard or Tables however you like
