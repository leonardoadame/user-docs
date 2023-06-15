# Insights setup: Image scanning

To determine the risk factors and prioritize your Code, Open Source, and Container issues, you must scan your container images using [Snyk Container](../../../scan-containers/).&#x20;

The container image is at the center of the application model powering Insights. A container image includes your source code and dependencies, and it is deployed to your running environment, enabling Insights to use the container image to bridge the development and deployment states.\
\
Insights will identify any deployed container images using the [Kubernetes Connector](insights-setup-kubernetes-connector.md) in the previous setup step and compare the deployed container images to the list of scanned images you have scanned using [Snyk Container](../../../scan-containers/).&#x20;

{% hint style="info" %}
Snyk recommends that you scan each image using at least one of the Snyk Container integrations.
{% endhint %}

## Snyk Container scanning with the CLI

For details, see [Snyk CLI for container security](../../../scan-containers/snyk-cli-for-container-security/).

To ensure the names match, specify the full name of the image as referenced in your Kubernetes deployment.&#x20;

For example: **$ snyk container monitor gcr.io/my-company/my-image:latest**

## Snyk Container registry scanning

For details, see [Snyk Container - Integrations](../../../scan-containers/snyk-container-integrations/).

The names will match if you are importing images to Snyk from the same container registry that you are referencing in your Kubernetes deployments.

## Snyk Container scanning with Kubernetes integration

For details, see [Kubernetes integration](../../../scan-containers/kubernetes-integration/).

The names of the container images will match, as the deployed image is scanned by Snyk and created as a Project.

{% hint style="warning" %}
To ensure you have set up your Kubernetes connector properly, navigate to the **Data** tab on the **Insights** page and check the **Image coverage** section to view the data that Insights has access to.
{% endhint %}
