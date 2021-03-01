# Update containers on a Synology NAS

## Via webbgui

1. Click the `Docker` app in Synology DSM

2. Click the `Registry` tab

3. Search for the container you wish to update

4. Select your container in the list and click `Download` in the topbar

5. Choose tag in the dropdown list then click `Select`

6. After the container has been downloaded, go to the `Container` tab and stop the your container

7. Stop the container you want to update

8. `Select` the container and, using the dropdown list, choose `Clear`

9. Start the new container.

## Via CLI
You can access your container id & image name with the `$ sudo docker ps` command

1. `ssh` to your Synology NAS

2. `Pull` down the latest image

   ```sh
   $ sudo docker pull <IMAGE-NAME:TAG>
   ```

3. `Stop` your container

   ```sh
   $ sudo docker stop <CONTAINER-ID>
   ```

4. `Clear` your container

   ```sh
   $ sudo docker container rm <CONTAINER-ID>
   ```

5. `Run` your container

   ```sh
   $ sudo docker run <CONTAINER-ID>
   ```