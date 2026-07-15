# ServiceNowDocs

ServiceNow AI Platform™ product documentation with the content format optimized for AI Agent consumption.

> NOTE: This repository does not contain any media objects (images, etc.). As it is intended for LLM consumption and not human viewing, images are omitted. Human readers can find all images and other media objects at the official [product documentation site](https://www.servicenow.com/docs).

Australia release family documentation.

## Refresh cadence

This repository is updated whenever the ServiceNow AI Platform documentation
is republished to [the product documentation site](https://www.servicenow.com/docs),
normally at least monthly, sometimes more often.

## Tips

* Point your AI at `llms.txt` and it should be able to find everything, i.e. "Read https://github.com/ServiceNow/ServiceNowDocs/edit/australia/llms.txt and explain AI Control Tower".
* **Windows Users:** If you encounter "filename too long" errors when cloning, run:
  ```
  git config --global core.longpaths true
  ```

## Change log
- __09 July 2026__:
  * July docs refresh
- __25 June 2026__:
  * Fixed build bug resulting in many empty markdown files. Any remaining empty markdown files are the result of other minor build issues that will be resolved as time allows.
- __24 June 2026__:
  * Reverted URLs to May refresh versions to match doc site URls.
- __21 June 2026__:
  * Issues 8 and 17: All links within and between publications are absolute URLs to the GitHub raw format.
  * Issue 16: Media references are rendered as annotations indicating an omitted image with any alternative text retained.
  * Issue 12: Filenames differing only in case resolved.
  * Issue 11: Canonical URL metadata added.
- __10 May 2026__ Republished Australia content to correct truncated index.md files, fix cross-publication links.
- __29 April 2026__ Initial publication of Australia family content
- __23 April 2026__ Repository created.
