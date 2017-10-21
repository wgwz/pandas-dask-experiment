So far this isn't really doing anything to interesting.
But if you want to get a docker container up and running with `pandas`
You can do this:

    cd how-pandas-fails
    docker-compose build
    docker-compose run pandas1 python

After that you'll have a Python 3 terminal up and running with the 
the latest version of Pandas running.

So you will be able to do this now:

    import pandas as pd

And to see the container running: 

    docker container ls

And to open a bash shell in that container:

    docker exec -it <container-id> bash

(where <container-id> is the long hash output in `docker container ls`.)

From the bash terminal you can inspect the Python process with usual tools:

    top
