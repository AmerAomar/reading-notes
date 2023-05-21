# Reading class 16

## What is serverless? [link](https://www.ibm.com/topics/serverless)

**What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?**

1. Serverless computing is a cloud computing model where the cloud provider manages the infrastructure and dynamically allocates computing resources to run applications on behalf of the developers. Here are the key characteristics of serverless computing and how it differs from traditional server-based architectures:

2. No server management: In serverless computing, developers do not have to worry about managing servers or infrastructure. The cloud provider abstracts away the underlying hardware, operating systems, and server configurations. Developers can focus solely on writing and deploying code.

3. Event-driven architecture: Serverless applications are typically event-driven. They are triggered by events such as HTTP requests, database updates, message queue events, or scheduled events. When an event occurs, the cloud provider automatically scales up the necessary resources to handle the event and executes the associated code.

4. Pay-per-use billing: Serverless computing follows a pay-per-use pricing model. Developers are only billed for the actual execution time and resources consumed by their code. The cloud provider dynamically scales the resources up and down based on the incoming workload. This allows for efficient resource utilization and cost optimization.

5. Automatic scalability: Serverless platforms automatically scale the resources allocated to an application based on the incoming workload. When the workload increases, the cloud provider provisions additional resources to handle the demand. Conversely, when the workload decreases, resources are scaled down to minimize costs. This automatic scalability eliminates the need for capacity planning and ensures optimal performance.

6. Micro-billing and granular scaling: Serverless platforms can scale at a very fine-grained level, executing code in small units called functions. Each function represents a discrete piece of functionality. As events trigger the execution of these functions, the cloud provider charges only for the actual function invocations and the resources consumed during their execution.

Stateless execution: Serverless functions are stateless by design. They are intended to perform a specific task or function and do not maintain persistent connections or store session information. Any required data or state is typically stored in external services such as databases or object storage.

------------------

## Vercel - Get Started [link](https://vercel.com/docs/concepts/get-started/deploy)

**How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?**

To get started with Vercel and deploy a serverless function, you can follow these main steps:

Sign up for a Vercel account: Visit the Vercel website (https://vercel.com) and sign up for an account. You can use your GitHub, GitLab, or Bitbucket account for a seamless sign-up process.

Install the Vercel CLI (Command-Line Interface): The Vercel CLI allows you to deploy and manage your projects from the command line. Install the Vercel CLI by following the instructions provided in the Vercel documentation for your specific operating system.

Prepare your project: Ensure that your project is ready for deployment. This includes organizing your project files and dependencies appropriately. Make sure you have a serverless function that you want to deploy.

Initialize your project: Open your project directory in the terminal and run the command vercel init. This command will initialize your project and create a vercel.json file that contains the deployment configuration.

Configure your project settings: Customize your project settings in the vercel.json file. You can specify details such as the build command, output directory, environment variables, and more.

Deploy your project: Run the command vercel in your project directory to start the deployment process. The Vercel CLI will build and package your project, and then deploy it to the Vercel platform. It will provide you with a unique URL for your project.

Test and verify your deployment: Once the deployment is complete, visit the provided URL to test and verify that your serverless function is working as expected.

Customize your deployment: Vercel offers various customization options to enhance your deployment. You can configure custom domains, SSL certificates, environment variables, routing, and more. Refer to the Vercel documentation for more details on these advanced deployment options.

Continuous deployment: Vercel integrates with popular version control systems such as Git. You can set up continuous deployment to automatically trigger deployments whenever you push changes to your repository. This ensures that your deployments stay up to date with your code changes.

Vercel provides a user-friendly interface and powerful deployment capabilities for serverless functions and static websites. The documentation available on their website provides detailed instructions and examples to guide you through the process.

------------------

## Requests [link](https://realpython.com/python-api/)
**What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?**

The Requests library is a popular Python library that simplifies the process of making HTTP requests and interacting with APIs. It provides a higher-level interface compared to Python's built-in urllib module, making it easier to send HTTP requests, handle responses, and work with JSON data.

To use the Requests library, you first need to install it. You can install it using pip, the package installer for Python, by running the following command:

```python
pip install requests
```

Once installed, you can import the Requests library into your Python script and start making HTTP requests.

Here's an example of a basic GET request using the Requests library:

```python
import requests

# Send a GET request to a URL
response = requests.get("https://api.example.com/data")

# Check the response status code
if response.status_code == 200:
    # Request was successful
    data = response.json()  # Get the response data as JSON
    print(data)
else:
    # Request failed
    print("Request failed with status code:", response.status_code)
```

In this example, we import the requests module and use the get function to send a GET request to the specified URL ("https://api.example.com/data"). The response from the server is stored in the response object.

We can then check the status_code attribute of the response to determine if the request was successful (status code 200). If it was successful, we can access the response data using the json method, which parses the response content as JSON and returns it as a Python object (e.g., a dictionary).

If the request fails (e.g., due to a server error or invalid URL), the status code will indicate the error. In the example, we print the error message along with the status code.

The Requests library supports other HTTP methods like POST, PUT, DELETE, etc., and provides additional features for handling headers, authentication, cookies, and more. The library documentation (https://docs.python-requests.org/) offers detailed information and examples on how to utilize these functionalities.
