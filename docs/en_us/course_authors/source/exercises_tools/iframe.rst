.. _IFrame:

##################
IFrame Tool
##################

An IFrame allows you to integrate ungraded exercises and tools from any Internet site into the body of your course. The IFrame appears inside an HTML component, and the exercise or tool appears inside the IFrame.

IFrames are well-suited for third-party tools that demonstrate a concept but that won't be graded or store student data. 

For more information about IFrames and their attributes, see the `IFrame specification <http://www.w3.org/wiki/HTML/Elements/iframe>`_.

.. image:: /Images/IFrame_1.png
  :alt: IFrame tool showing a Euler line exercise
  :width: 500

.. image:: /Images/IFrame_2.png
   :alt: IFrame tool showing the Euler exercise in action
   :width: 500

****************************
Create an IFrame Tool
****************************

To add an exercise or tool in an IFrame, you'll create an IFrame HTML component and add the URL of the page that contains the exercise or tool to the component. You can also add text and images both before and after the IFrame.

.. note:: For an IFrame to appear in all browsers, the URL of the page that contains the exercise or tool must start with ``https`` instead of ``http``.

#. Under **Add New Component**, click **html**, and then click **IFrame**.

#. In the new component that appears, click **Edit**.

#. In the component editor, click **HTML** in the toolbar.

#. In the HTML source code editor, locate the following HTML (line 7):

   .. code-block:: html

      <p><iframe src="https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html" width="402" height="402" marginwidth="0" marginheight="0" frameborder="0" scrolling="no">You need an iFrame capable browser to view this.</iframe></p>

5. Replace the default URL (**https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html**) with the URL of the page that contains the exercise or tool. This URL must start with **https**.

#. Specify any other settings that you want in the code for the IFrame. For more information, see :ref:`IFrame Settings`.

   .. note:: The text between the opening and closing ``<iframe>`` tags is the text that appears if a student uses a browser that does not support IFrames. You can leave this text as-is or change it.

7. Click **OK** to close the HTML source code editor and return to the Visual editor.

#. Replace the default text with your own text.

#. Click **Save**.

.. _IFrame Settings:

======================
IFrame Settings
======================

.. list-table::
   :widths: 20 80
   :header-rows: 1
 
   * - Attribute
     - Description
   * - **src** 
     - Specifies the URL of the page that contains the exercise or tool.
   * - **width** and **height**
     - Specify the width and height of the IFrame, in pixels. The width and height that you set for an IFrame must always be at least as large as the exercise or tool that it contains. 
   * - **marginwidth** and **marginheight**
     - Specify the size of the space between the edges of the IFrame and your exercise or tool, in pixels.
   * - **frameborder** 
     - Specifies whether a border appears around your IFrame. If the value is 0, no border appears. If the value is any positive number, a border appears.
   * - **scrolling** 
     - Specifies whether users can use a scrollbar to see all of your content if your IFrame is smaller than the exercise or tool it contains. 

For example, compare how the different settings in each of the examples below affects the IFrame. 

.. code-block:: html

      <p><iframe src="https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html" width="442" height="200" marginwidth="20" marginheight="20" frameborder="1" scrolling="yes">You need an iFrame capable browser to view this.</iframe></p>

.. image:: /Images/IFrame_3.png
   :alt: IFrame with only top half showing and vertical scroll bar on the side
   :width: 500


.. code-block:: html

      <p><iframe src="https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html" width="550" height="250" marginwidth="30" marginheight="60" frameborder="1" scrolling="no">You need an iFrame capable browser to view this.</iframe></p>

.. image:: /Images/IFrame_4.png
   :alt: 
   :width: 500



For more information about IFrame attributes, see the `IFrame specification <http://www.w3.org/wiki/HTML/Elements/iframe>`_ and `The IFrame Element <http://www.w3.org/TR/html5/embedded-content-0.html#the-iframe-element>`_.
