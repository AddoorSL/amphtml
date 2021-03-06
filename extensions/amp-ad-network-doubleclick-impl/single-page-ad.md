<!---
Copyright 2018 The AMP HTML Authors. All Rights Reserved.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS-IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
-->

# Single Page Ads

A single page ad allows an ad creative to appear as a full page, dynamically interleaved, within the pages of an AMP story. For more information about AMP stories, see [here](https://github.com/ampproject/amphtml/blob/master/extensions/amp-story/amp-story-ads.md).

## Adding a Single Page Ad to Your Story

Single page ads are similar to regular DoubleClick ads, but must be tagged as script elements within an `<amp-story-auto-ads>` element as follows:

```html
<amp-story-auto-ads>
  <script type="application/json">
    {
      "ad-attributes": {
        "type": "doubleclick",
        "data-slot": "/30497360/a4a/amp_story_dfp_example"
      }
    }
  </script>
</amp-story-auto-ads>
```

You __cannot__ use an `<amp-ad>` element to display a single page ad within a story.

## Single Page Ad Creatives

Single page ad creatives must contain two meta tags: one to specify the [call-to-action enum](https://github.com/ampproject/amphtml/blob/master/extensions/amp-story/amp-story-ads.md#cta-ad), and one to specify the outlink URL. E.g.,

```html
<meta name="amp-cta-url" content="https://www.example-ads.com/landing?q=123">
<meta name="amp-cta-type" content="EXPLORE">
```

See the above link for allowed call-to-action buttons. By design, these will be the only clickable elements of the creative unit. This means that while things like AMP carousels are allowed within a single page story ad, they will not be clickable.

#### <a href="amp-ad-network-doubleclick-impl-internal.md">Back to DoubleClick</a>
