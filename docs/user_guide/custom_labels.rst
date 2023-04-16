Add custom labels to your org using a Python dictionary
------------------
To quickly add custom labels to your org using a Python dictionary, you can use the simple_salesforce library which provides a simple way to interact with the Salesforce API. Here's an example of how you can create custom labels using a Python dictionary:

.. code-block:: python
    from simple_salesforce import Salesforce
    sf = Salesforce(username='your-username', password='your-password', security_token='your-token')

    # Define the custom labels as a Python dictionary
    custom_labels = {'LABEL_NAME_1': 'Label Value 1', 'LABEL_NAME_2': 'Label Value 2', 'LABEL_NAME_3': 'Label Value 3'}

    # Loop through the dictionary and create the custom labels
    for label_name, label_value in custom_labels.items():
        sf.CustomLabel.create({'FullName': label_name, 'Value': label_value})


.. code-block:: python

    from simple_salesforce import Salesforce
    sf = Salesforce(username='your-username', password='your-password', security_token='your-token')
    # Define the custom labels as a Python dictionary
    custom_labels = {'LABEL_NAME_1': 'Label Value 1', 'LABEL_NAME_2': 'Label Value 2', 'LABEL_NAME_3': 'Label Value 3'}
    # Loop through the dictionary and create the custom labels
    for label_name, label_value in custom_labels.items():
        sf.CustomLabel.create({'FullName': label_name, 'Value': label_value})
        
In this example, we first import the Salesforce class from the simple_salesforce library and create a new Salesforce instance by passing in our credentials.
Next, we define the custom labels as a Python dictionary where the key is the label name and the value is the label value.

Finally, we loop through the dictionary using the items() method and create the custom label in Salesforce by calling the create() method on the CustomLabel object. We pass in a dictionary with two keys: FullName which is the label name and Value which is the label value.

This is a quick and easy way to create custom labels in Salesforce using Python. Note that you'll need to have the appropriate permissions to create custom labels in your org.
