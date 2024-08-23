---
title: Step 3. Running the container
---

Now that we have the container definition, we can launch it.

1. Make sure that Docker Desktop is running.
2. Open the command line in the `node-dev` directory.
3. Build and run the container by executing the following command:  

```bash
$ docker compose up
``` 

Now, if you open the link `localhost:3000` in your web browser, you will see the message "Test server is running!".

Try changing this text on your local machine and reload the page. After some delay, you will see the new text in the browser.

Now you can develop and test your application inside a container without worrying about conflicting dependencies or inconsistent environment.

You can also easily share your container with other members of your development team.