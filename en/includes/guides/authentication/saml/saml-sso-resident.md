# Configure SAML Web SSO for your organization

When WSO2 Identity Server acts as a SAML Identity Provider (IdP), it manages the authentication of users and issues SAML assertions to trusted Service Providers (SPs). You can configure how this behavior works by adjusting the SAML Web Single Sign-On (SSO) settings.

To do so, follow the steps below:

1. On the {{product_name}} Console, go to **Login & Registration**.

2. Under **Single Sign-On (SSO) Settings**, click **SAML2 Web SSO Configuration**.

3. Configure the following properties.

    <img src="{{base_path}}/assets/img/guides/authentication/saml2-web-sso-resident.png" width="600" alt="SAML2 Web SSO configurations"/>

| Field                     | Description                                                                 | Sample/Default Value |
|--------------------------|-----------------------------------------------------------------------------|----------------------|
| **Enable Metadata Signing**  | Enable or Disable metadata signing. | `false` |
| **Metadata Validity Period** | The duration (in minutes) for which the metadata will remain valid before it should be refreshed. | `60` |

4. Click **Update** to save the changes.

{% if product_name == "Asgardeo" %}
!!! note
    You can download the SAML2 metadata by accessing the URL: `https://api.asgardeo.io/t/<org_name>/identity/metadata/saml2`.

{% else %}
!!! note
    You can download the SAML2 metadata by starting the server and downloading the SAML2 metadata by accessing this URL: `https://localhost:9443/identity/metadata/saml2`.

{% endif %}
