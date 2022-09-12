# Changelog

## 12/09/2022

* Updated the Order Notes parser to allow for shortform aliases (1, 2, or 3-letters) for each key.
* Updated the Image Number parser to allow for various *selector* types, such as a *single* (`xxxx`), *range* (`xxxx-yyyy`), *forward* (`xxxx+y`) and *negated* (`!xxxx`) selector, and introduced the ability to include multiple terms (`xxxx, xxxx-yyyy, xxxx+y ...`)
* Added a 120 minute buffer period for searching through photos, as the 10 minute buffer is potentially too short to be meaningful in the automation.
* Improved some of the error messages' and warning messages' specificity.
* Increased the maximum Step Function runtime to 60 minutes.
