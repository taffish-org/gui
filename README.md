# taf-gui

- This is a taf-app(taf-tool), you can use taffish(https://www.taffish.com) to use this taf-app.
- This app is from VNC and noVNC.

Use VNC and no VNC to support gui for taf apps.

## gui:v1.0.0 -- Use gui in your browser (an examply by taf-juicebox:v3.1.4 [port :: 5802])

For the gui mode, we do it together with [noVNC](https://github.com/novnc/noVNC) through VNC, which makes it possible to access the gui version of taf-apps through a browser, as shown in the following tutorials:

### 1. Run the following command on the CLI:

  ```bash
  taf update
  taf install -y gui  # or any gui-taf-app, such like taf-pymol, taf-juicebox, ...
  # restart terminal or [$ source ~/.bashrc] or [$ source ~/.zshrc] ...
  taf-gui --passwd 12345678 --port 5809
  # --c only support docker and podman, chose yours              [default podman>docekr]
  # --passwd will be used when you try to connect the gui        [default 12345678]
  # --port will be used when you try to connect the gui          [default 5809]    # it will only be set once when you first run taf-gui
  ```

### 2. Check the output and the URL

  Wait for the run to finish, check for errors, and if everything is fine, look at the end of the output, you can get a web address, for example:
  
  ```
  >>> TAFFISH-GUI ===> http://localhost:5809/vnc.html <<<
  ```

  Copy the URL and open it in your browser to access taffish-gui:
  
  <img width="1446" alt="image" src="https://github.com/user-attachments/assets/ea6fab03-6ca5-4204-ad6f-b3b1fcf18eff" />
  
### 3. Enter the password and enter the GUI interface (the password is the --passwd set at runtime, the default is 12345678)

  <img width="1448" alt="image" src="https://github.com/user-attachments/assets/528e28e8-a082-4fd3-ae43-190b0497cbae" />
  
### 4. Open the terminal in the GUI and enter the gui command to open your app by gui in the GUI interface

  <img width="1449" alt="image" src="https://github.com/user-attachments/assets/fe2cd3d5-1a14-43ee-a3b7-42bd2bebe629" />
  
### 5. Use juicebox-gui

  <img width="1450" alt="image" src="https://github.com/user-attachments/assets/aeceff72-80ed-4cf9-b3c4-b77f851bd2e7" />
  
  <img width="1449" alt="image" src="https://github.com/user-attachments/assets/65817b22-18f0-4b04-84d6-1337479362b3" />
  
  <img width="1449" alt="image" src="https://github.com/user-attachments/assets/9a909b8e-34f8-4d1b-846e-18351df2cce0" />
  
  Note:
  - By default, the /root/ path in the container needs to be retrieved from the global path /home/$USER
  - For the remote server, you can change the localhost in the URL to the server IP to access the taffish-gui on the remote server
  - Only a single screen is created for the same port/container service, and different accesses share the same screen. If you want to start a new service, please open a new docker/podman container(use another user to run taf-gui) and select a new port
