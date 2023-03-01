+++
title = "Configure Provisioning"
chapter = false
weight = 43
+++

1. Go to the **AWS Management console** and open the **IAM Identity Center**.
![AWS IAM Identity Center User portal](/images/go_to_aws_sso.png)

2. Go to **Settings** and **Enable** Automatic provisioning.
![Enable Provisioning](/images/192_enable_provisioning.png)

3. Copy the values of **SCIM endpoint** and **Access token**.
![Copy SCIM Endpoint](/images/191_copy_scim_endpoint.png)

4. Go to Okta and select the tab **Provisioning**. Click on **Configure API Integration**.
![Configure API Integration](/images/193_configure_api_integration.png)

5. Paste the two copied values and click on **Test API Credentials**. When you copy the URL, make sure there is no **/** at the end or link validation in Okta will fail. Click on **Save**.
![Provisioning Configuration](/images/194_provisioning_configuration.png)

6. In the **Provisioning** tab make sure that **To App** is selected. In the top right corner click on **Edit** and select **Enable** for **Create, Update and Deactivate** Users. Click on **Save**.
![Configure Provisioning](/images/200_enable_provisioning.png)