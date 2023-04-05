# Upterm Github job

If you need to enter your Github runner container and be able to develop/debug in that environment, 
one way to do this is by using upterm. Upterm is an open-source solution for sharing terminal sessions 
instantly over the public internet via secure tunnels. <br><br>
In order to do this, just copy the Github job in `upterm-connect.yml` file, in your Github workflow.
The next time you run the pipeline, when it starts executing the *Upterm connect* job, it will give you a 
connection string in the job log output through which you can connect through SSH. The script used in the 
`upterm-connect.yml` can be re-used for other CI tools as well. <br>
The advantage of this not being in a Github action, is that it is flexible to be easily re-arranged for 
anyone's needs. <br><br>
The technical implementation was inspired by: <br>
https://github.com/lhotari/action-upterm
