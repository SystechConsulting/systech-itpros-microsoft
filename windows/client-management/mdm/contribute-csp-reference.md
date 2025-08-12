---
title: Contributing to CSP reference articles
description: Learn more about contributing to the CSP reference articles.
ms.date: 07/18/2023
ms.topic: reference
ms.localizationpriority: medium
---

# Contributing to the CSP reference articles

CSP reference articles are automatically generated using the [device description framework (DDF)](configuration-service-provider-ddf.md) v2 files that define the CSP. When applicable, the CSP definition includes a mapping to a group policy. The automation uses this mapping, when possible, to provide a friendly description for the CSP policies.

> [!IMPORTANT]
> Each automated CSP article provides editable sections to provide additional information about the CSP, the policies within the CSP, and usage examples. Any edits outside the designated editable sections are overwritten by the automation.

## CSP article structure

Each automated CSP article is broken into three sections.

> [!NOTE]
> To view these sections, visit the article that you want to update, then select the **Pencil** icon.
> :::image type="content" source="images/csp-contribute-link.png" alt-text="Screenshot showing the Pencil icon to edit a published article":::

1. **Header**: The header includes the CSP name, and provides an editable section where additional information about the CSP can be provided.

   :::image type="content" source="images/csp-header.png" alt-text="Screenshot of the CSP header section":::

1. **Policies**: The policies section contains a list of policies, where each policy has an editable section for providing additional information and examples.

   :::image type="content" source="images/csp-policy.png" alt-text="Screenshot of the CSP policy section":::

1. **Footer**: The footer indicates the end of the CSP article, and provides an editable section where more information about the CSP can be provided.

   :::image type="content" source="images/csp-footer.png" alt-text="Screenshot of the CSP footer section":::

## Provide feedback on documentation

CSP articles are automated using the DDF v2 and ADMX files, which are part of the Windows codebase. Intune settings catalog also uses the DDF v2 files to present the settings and help text. As such, the feedback for these articles is best addressed when submitted directly to the engineering team using [Feedback Hub app](#send-feedback-with-the-feedback-hub-app). CSP reference articles and the Intune settings catalog are updated periodically using the latest copy of DDF v2 files, and benefit from the feedback addressed by the engineering team.

Automated CSP articles also contain [editable content](#csp-article-structure), which is preserved by the automation. For any feedback about the editable content, use the [Microsoft Learn documentation contributor guide][CONTRIB-1].

:::image type="content" source="images/csp-feedback-flow.svg" alt-text="Diagram showing the feedback flow for CSP articles":::

Use these sections to determine where you should submit feedback.

### Feedback for policy description

Policy descriptions are sourced from DDF or ADMX files and are located within the `<[CSP-Name]-Description-Begin>` section for the policy in the markdown file. `<[CSP-Name]-Description-Begin>` also includes a reference to the source that was used to provide the policy description.

- `Description-Source-ADMX` or `Description-Source-ADMX-Forced`: The description was captured from the group policy that the CSP setting maps to. If this description is incorrect, [Send feedback with the Feedback Hub app](#send-feedback-with-the-feedback-hub-app).
- `Description-Source-DDF` or `Description-Source-DDF-Forced`: The description was captured from the DDF file that defines the CSP. If this description is incorrect, [Send feedback with the Feedback Hub app](#send-feedback-with-the-feedback-hub-app).
- `Description-Source-Manual-Forced`: The description is defined in the automation code. If this description is incorrect, [submit an issue](/contribute/#create-quality-issues).

Any additional information about the policy setting can be provided in the `[Policy-Name]-Editable-Begin` section that immediately follows the `<[CSP-Name]-Description-End>` section. This section allows further expansion of the policy description, and is generated manually. For any feedback for the editable content, use the [Microsoft Learn documentation contributor guide][CONTRIB-1] to update the section or submit an issue.

### Feedback for policy examples

Policy examples aren't provided by the automation. Each policy node in the markdown file includes a `[Policy-Name]-Examples-Begin` section that contains the examples. If the example is incorrect or needs to be updated, use the [Microsoft Learn documentation contributor guide][CONTRIB-1] to update the example or submit an issue.

### Feedback for policy applicability

Policy applicability is defined in the DDF v2 file for the CSP. Each policy node in the markdown file includes a `[Policy-Name]-Applicability-Begin` section that contains the operating system applicability.

If it's incorrect or needs to be updated, [Send feedback with the Feedback Hub app](#send-feedback-with-the-feedback-hub-app).

### Feedback for policy allowed values

Policy allowed values are defined in the DDF v2 file for the CSP. When applicable, each policy node in the markdown file includes a `[Policy-Name]-AllowedValues-Begin` section that contains a table that describes the allowed values for the policy.

If these values are incorrect or need to be updated, [Send feedback with the Feedback Hub app](#send-feedback-with-the-feedback-hub-app).

### Feedback for group policy mapping

Group policy mappings are defined in the DDF v2 file for the CSP. When applicable, each policy node in the markdown file includes a `[Policy-Name]-AdmxBacked-Begin` or `[Policy-Name]-GpMapping-Begin` section that contains the group policy mapping.

If this mapping is incorrect, [Send feedback with the Feedback Hub app](#send-feedback-with-the-feedback-hub-app).

### Other feedback

For any other feedback, use the [Microsoft Learn documentation contributor guide][CONTRIB-1].

## Send feedback with the Feedback Hub app

The Feedback Hub app lets you tell Microsoft about any problems you run into while using Windows. For more information about using Feedback Hub, see [Send feedback to Microsoft with the Feedback Hub app](https://support.microsoft.com/windows/send-feedback-to-microsoft-with-the-feedback-hub-app-f59187f8-8739-22d6-ba93-f66612949332). When you submit feedback for CSP documentation with the Feedback Hub app, use these steps:

1. **Enter your feedback**: Prefix your feedback summary with `[CSP Documentation]` in the **Summarize your feedback** section. Add details about the feedback, including the link to the CSP article.
1. **Choose a category**: Select **Security and Privacy > Work or School Account** as the category.
1. **Find similar feedback**: Select an existing feedback that matches your feedback, if applicable.
1. **Add more details**: Select **Other** as the subcategory.
1. Select **Submit**.

## Related articles

- [Contributor guide overview][CONTRIB-1]

<!-- Links -->

[CONTRIB-1]: /contribute
