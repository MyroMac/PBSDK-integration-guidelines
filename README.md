# PBSDK-integration-guidelines

----------

Example of Acceptable Code
-------------------
Please see the following repo for an example of acceptable code:
https://github.com/MyroMac/PBAddPartyFavor

Steps for PBSDK Integration
-------------------
1. update podspec to make PBUIElements a dependency (this will allow us to do use PBBaseViewController in step 2)
2. update podspec and add xcassets as one of the file types that the resource_bundles includes, see line 36 of PBPartyDetails.podspec
3. create Images.xcassets in Assets folder and create an image entry for the view controller’s loading image
4. override loaderImage in the view controller (see loaderImage method of PBAddPartyFavorViewController)
5. make main view controller of the pod a subclass of PBBaseViewController to have needed methods for PBSDK Integration (see how PBAddPartyFavorViewController is a subclass of PBBaseViewController)
6. at the end of viewDidLoad we will download data from the API (see end of viewDidLoad in PBStockPartyFavorsViewController class)
7. display loader via method in PBBaseViewController method and download the data using the class/method listed above
8. hide loader and display the data accordingly
