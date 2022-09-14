# Changelog

## 14/09/2022

* Increased SmugMug upload retry count to 6.
* Added 15s/6r/3x back-off interval for SmugMug upload process.
  * The back-off times are:
  * 0:00 / 0:15 / 1:00 / 3:15 / 10:00 / 30:15
* Added a retrier for the Dropbox image search with an 80s/8r/2x back-off interval.
  * The back-off times are:
  * 0:00 / 1:20 / 4:00 / 9:20 / 20:00 / 41:20 / 1:24:00 / 2:49:00
* Removed the fallback parser for order notes - it now fails with a MissingNotesError if it can't parse relevant KV.


## 12/09/2022

* Updated the Order Notes parser to allow for shortform aliases (1, 2, or 3-letters) for each key.
* Updated the Image Number parser to allow for various *selector* types, such as a *single* (`xxxx`), *range* (`xxxx-yyyy`), *forward* (`xxxx+y`) and *negated* (`!xxxx`) selector, and introduced the ability to include multiple terms (`xxxx, xxxx-yyyy, xxxx+y ...`)
* Added a 120 minute buffer period for searching through photos, as the 10 minute buffer is potentially too short to be meaningful in the automation.
* Improved some of the error messages' and warning messages' specificity.
* Increased the maximum Step Function runtime to 60 minutes.
