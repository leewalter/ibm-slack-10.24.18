# Create and Populate Cloudant Database

## Launch IBM Function

1. Sign into [IBM Cloud](https://console.bluemix.net).

    ![IBM Sign up](assets/cloudant-start.jpg)

2. Click on `Catalog` and enter `function` in the search field. Select the `Functions` service by IBM.
  
    ![IBM Sign up](assets/ibm-function-catalog.jpg)

3. Launch the IBM Function page by clicking on `Start Creating`.
  
    ![IBM Sign up](assets/ibm-function-launch.jpg)

4. If you get the error below, close the dialog and pick `US South` 

    ![IBM Sign up](assets/ibm-function-launch-error.jpg)

    ![IBM Sign up](assets/ibm-function-launch-error-fix.jpg)
## Create an action to get a random talk

5. Click `Create` to create a new action.

    ![IBM Sign up](assets/ibm-function-home.jpg)

6. Give the action the name `confbot-get-random-talk`.

    ![IBM Sign up](assets/ibm-function-random-create.jpg)

7. Create a package with the name `confbot` instead of picking the default package.

    ![IBM Sign up](assets/ibm-function-create-package.jpg)

8. Click on `Create` to go into the new action.

    ![IBM Sign up](assets/ibm-function-random-code.jpg)

9. Click on `Parameters` to add the cloudant username and password to the action. You can get your username, and password from the `cloudant/.env.json` file you created in the previous section. Alternatively, you can go to your Dashboard and copy them from the `service credentials` tab.

    ![IBM Sign up](assets/ibm-function-cloudant-parameters.png)

10. Add three values: user, password and database as shown below.

    ![IBM Sign up](assets/ibm-function-random-parameter.png)

11. Click on `code` and add the contents of the file `ibm-function/confbot-get-random-talk.js` to the action.

    ![IBM Sign up](assets/ibm-function-get-random-code.jpg)

12. Click on `invoke` to run the function. You should see an author in the console.

    ![IBM Sign up](assets/ibm-function-get-random-invoke.jpg)

## Create an action to get three talks for a given `tag/track`

13. Click `Actions` to go to the main page.

    ![IBM Sign up](assets/ibm-function-go-home.jpg)

    You should see the function you created in the previous step.
    
    ![IBM Sign up](assets/ibm-function-go-home-2.jpg)


14. Click on `Create` to create a new action. Pick `Create Action`. 

    ![IBM Sign up](assets/ibm-function-new-action.jpg)

15. Give your action the name `confbot-get-track-talks`. Pick `confbot` as the enclosing package.

    ![IBM Sign up](assets/ibm-function-track-talks-create.jpg)

16. Once you click `Create`, you will be brought into the action.

    ![IBM Sign up](assets/ibm-function-track-talks-create-2.jpg)

17. Click on params and set the following.

    ![IBM Sign up](assets/ibm-function-track-talks-params.png)

18. Click on `code` and add the contents of the file `ibm-function/confbot-get-track-talks.js` to the action.

    ![IBM Sign up](assets/ibm-function-track-talks-code.jpg)

19. Click on `invoke` to run the function. You should see three talks with the tags `scala` in the output.

    ![IBM Sign up](assets/ibm-function-track-talks-invoke.jpg)

### [Go back to main page](README.md)

