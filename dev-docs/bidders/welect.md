---
layout: bidder
title: Welect
description: Prebid Welect Bidder Adaptor
pbjs: true
biddercode: welect
media_types: no-display, video
userIds: false
tcfeu_supported: true
gvl_id: 282
gpp_sids: tcfeu
usp_supported: false
coppa_supported: false
schain_supported: false
dchain_supported: false
safeframes_ok: false
fpd_supported: false
floors_supported: false
ortb_blocking_supported: false
multiformat_supported: will-bid-on-one
privacy_sandbox: none
sidebarType: 1
---

### Note

The Welect bidder adapter requires setup and approval from the Welect team. Please reach out to [dev@welect.de](mailto:dev@welect.de) for more information.

### Bid params

{: .table .table-bordered .table-striped }
| Name | Description | Example | Type |
|---|---|---|---|
| `placementId` | an identifier for your placement, provided by Welect | `'exampleID'` | `string` |
| `cattax` | (optional) The content taxonomy used to describe the page's content. `'iab2'` and `'iab3'` for Context Taxonomies versions 2.x and 3.x by the IAB: [https://iabtechlab.com/standards/content-taxonomy/](https://iabtechlab.com/standards/content-taxonomy/) | `'iab2'` | `string` |
| `cat` | (optional) The content categories describing the page's content. | `["1", "10"]` | `array of strings` |

### Example Ad Unit Setup

```javascript
var adUnits = [
  {
    bidder: 'welect',
    params: {
      placementId: 'exampleId'
    },
    mediaTypes: {
      video: {
        context: 'instream',
        playerSize: [640, 360]
      }
    },
  };
];
```
