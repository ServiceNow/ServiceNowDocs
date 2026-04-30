---
title: Insert a header card in a Static Choice or Dynamic Choice control
description: When you create a Virtual Agent topic, you can include images and YouTube videos on Static Choice and Dynamic Choice user input controls.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a Virtual Agent topic, Getting started with Virtual Agent Designer, Building and deploying Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Insert a header card in a Static Choice or Dynamic Choice control

When you create a Virtual Agent topic, you can include images and YouTube videos on Static Choice and Dynamic Choice user input controls.

## Before you begin

Role required: virtual\_agent\_admin or admin

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer** and open a topic or [create a new one](create-virtual-agent-topic.md).

2.  On the Flow tab, drag a Static Choice or a Dynamic Choice user input control onto the canvas.

3.  On the Properties sheet, go to **Advanced \(optional\)**, and then expand the **Header card** section.

4.  Slide the **Insert** toggle switch to enable it.

    ![Header card section of Dynamic Choice user input control, with Insert toggle and Would you like help radio button enabled.](../images/va-insert-header-help-yes.png "Insert a header card")

5.  Under **Would you like help?**, select either **Yes** or **No, I will use a script**.

    -   If you selected **Yes**, select **Add card** and complete the following form fields.

<table id="table_j11_ghf_3cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Card type

</td><td>

Type of header card:-   Large image with text
-   Small image with text
-   Youtube Video Card
 The fields in the dialog box change according to your choice.

</td></tr><tr><td>

Title

</td><td>

Image or video title. You can enter it directly in the text field or use a data pill or script to provide the value.

</td></tr><tr><td>

Title Link

</td><td>

The URL to use for the video title hyperlink. You can enter it directly in the text field or use a data pill or script to provide the value. If this field is empty, the title displays as plain text.This field is only available for the YouTube video card option.

</td></tr><tr><td>

Description

</td><td>

Brief description of the image or video.

</td></tr><tr><td>

Image URL Link

</td><td>

URL link for the image. You can enter it directly in the text field or use a data pill or script to provide the value. You can also select **Upload Image** to upload the image.This field is only available for the large and small image card options.

</td></tr><tr><td>

Image alt text

</td><td>

Alternative, screen-readable text that describes the image. It’s used for accessibility programs.This field is only available for the large and small image card options.

</td></tr><tr><td>

Youtube Video ID

</td><td>

The alphanumeric string at the end of the YouTube URL. For example, in the URL `https://www.youtube.com/watch?v=AacDp2mUQ1I` the YouTube video ID is `AacDp2mUQ1I`.This field is only available for the YouTube video card option.

</td></tr></tbody>
</table>    -   If you selected **No, I will use Script**, select **Add script** to input a script to display your desired media, following the example in the script dialog box.

        ```
        function() {
            /*
                var cardName = "Large image with text";
                var cardData = {
                    title: 'Choose color',
                    description: 'choose the right color of the flowers in the image',
                    image: 'https://homepages.cae.wisc.edu/~ece533/images/tulips.png',
                    imageAlt: 'Choose color'
                }
                var template = "";
                if (vaSystem.isAMBClient(vaContext.deviceType))
                    template = vaSystem.fillTemplateFromData(cardName, JSON.stringify(cardData));
              return {
                  cardTemplate: template,
                  cardName: cardName,
                  cardData: JSON.stringify(cardData),
                  renderStyle: "card"
              };
            */
            }
        ```

6.  Select **Save**.


**Parent Topic:**[Create a Virtual Agent topic](create-virtual-agent-topic.md)

