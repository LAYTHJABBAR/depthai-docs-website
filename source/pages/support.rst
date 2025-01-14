Support
=======

Running into issues or have questions? We're here to help.

Creating Minimal Reproducible Example
#####################################

**Before requesting support, please also check** :ref:`Troubleshooting documentation page <Troubleshooting>`.

To help you debug the issue you have the fastest and most efficient please provide a Minimal Reproducible Example (**MRE**), docs on `how to create MRE here <https://stackoverflow.com/help/minimal-reproducible-example>`__.
This means everything, including **minimal script, required model .blobs, and any other assets**, should be compressed into single
file (zip/7z/tar) as the MRE. A few things to make sure before compressing files

#. That assets/model blobs are located at the right path.
#. Remove any unnecessary code: commented out code, and code that isn't relevant to the depthai/pipeline code (so host-side code).
#. Please provide **minimal code**. Main script should be as short as possible.

Besides MRE, please also provide the following information when you are requesting support:

* Name of the OAK camera (`all camera names here <https://docs.luxonis.com/projects/hardware/en/latest/>`__).
* The **Version of the deptahi** you are using. If it's not `the latest <https://github.com/luxonis/depthai-core/releases>`__, please also try updating the depthai version to the latest (``python -mpip install depthai -U``).
* Screenshot of your pipeline using the `Pipeline Graph tool <https://github.com/geaxgx/depthai_pipeline_graph>`__.
* If you are using an OAK PoE device:

  * We suggest first checking the `PoE troubleshooting page <https://docs.luxonis.com/projects/hardware/en/latest/pages/guides/getting-started-with-poe.html#poe-troubleshooting>`__.
  * **Bootloader version** you are using. You should have the latest bootloader version, see `OAK Device Manager <https://docs.luxonis.com/projects/api/en/latest/components/bootloader/#device-manager>`__ for checking/updating the bootloader version.

IP related issues
-----------------

If you are having an issue with an app that contains your (company's) **Intellectual Property**, eg. NN model or business logic, you should first
remove this IP before creating MRE:

- For **NN model**, replace your model with a public model. So if you trained an object detection NN, replace it with eg. public pretrained Mobilenet-SSD.
- For **business logic**, simply remove the code. MRE shouldn't contain much host-side code where your business logic would be.

Requesting support
##################

To **request support from our engineers**, please **open an issue on** our `DepthAI Github repository <https://github.com/luxonis/depthai/issues>`__.
You can also get support by:

- Joining our `Discord Community <https://discord.gg/luxonis>`__ for live assistance from us and developers like you
- Posting a message to `our forum <https://discuss.luxonis.com/>`__


Refunds and returns policy
##########################

At Luxonis, we are customer-focused. Our success is only possible if our customers believe in the value of our products. If for any reason you are not satisfied with your purchase, please let us know and we will make it right.

If you desire a refund, please contact support@luxonis.com with your order number and reason for the return. Refund requests within 60 days of the purchase date will be honored in full.

Shipping costs for returns within 60 days of purchase will be covered by Luxonis. Shipping costs for returns after 60 days from the purchase date will be born by the customer.

If a return is initiated because of damaged, defective, or incorrect goods, Luxonis will provide a replacement order at no cost to the customer.

Refunds will be processed within 14 days after the product has been returned.

.. include::  /pages/includes/footer-long.rst
