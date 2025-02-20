# How to connect REST API endpoint to Power BI

Here are step-by-step instructions for setting up your environment and configuring the necessary components to work with the Rest API Certificate and Bearer Token.

1. **Download and Install the Rest API Certificate**:
    - If you already have the certificate, simply download it and proceed to install the DER Certificate.
    - In case the certificate is not available:
        1. Access your Edge Manager portal: Edge Manager
        2. Navigate to the "Certificates" section.
        
        <img src="images/edge-admin-certificates.png" width=800><p>
        
        3. Generate the Rest API Certificate.
        
        <img src="images/rest-api-certificate.png" width=500><p>
        
        4. Download the certificate.
        
        5. Install it on your system.  
        
        <img src="images/install-rest-api-cert.png" width=500><p>


2. **Configure PowerBI for Rest API Access**:
    - Open PowerBI.
   
      <img src="images/power-bi-loader.png" width=800><p>

    - Go to **Home > Get Data > Web**.  
   
      <img src="images/power-bi-get-data.png" width=500><p>
    
    - A form will appear.  
    
      <img src="images/from-web-form.png" width=500><p>
    
    - Fill in the "URL Parts" with the appropriate details (e.g., `https://{edge ip}/edge/api/v1/ae`).

3. **Set HTTP Request Header Parameters**:
    - Add an HTTP request header parameter:
        - Name: `Authorization`
        - Value: `bearer {bearer_token}`

5. **Obtain the Bearer Token**:
    - Query the following URL: `https://{edge ip}/edge/api/v1/Login/GetAuthToken/profile`.
    - Provide the necessary body parameters (Username and Password) to authenticate and retrieve the bearer token.

6. **Copy access token from the result and paste it in the PowerBI form**:  
    <img src="images/bearer-token-sample.png" width=800><p>

    Replace the value of `Authorization` header `{bearer_token}` with the value of the result's `accessToken`. The value should the include `{}""` characters. Refer to the example below:

    **Example Result:**
    ```json
    {
       "accessToken": "abcdefg",
       "result": 1
    }
    ```
    **Example Authorization Value:**
    ```
    bearer abcdefg
    ```

Remember to replace `{edge ip}` with the actual IP address of your Edge server. These instructions will guide you in effectively using the Rest API and Bearer Token within PowerBI. 🚀

And thats it! You can now retrieve your data and connect it to Power BI in order to create reports, dashboards or tables.
