# Deploy a ML model on GCP with Streamlit
## 1. Set up a GCP VM
<p>Go to GCP Compute Engine --> VM instances --> Create Instance</p>
<img src="img/Picture1.png" width=600/>
<br>
<p>Set up the configuration like below, then create</p>
<img src="img/Picture2.png" width=600/>
<img src="img/Picture3.png" width=600/>

## 2. Connect to the VM
<p>Go to the local computer terminal, then the home directory </p>
<pre>cd ~</pre>
<p>Check if there is a .ssh folder</p>
<pre>ls .ssh</pre>
<p>If not, make one</p>
<pre>mkdir .ssh</pre>
<p>Then go to the .ssh folder</p>
<pre>cd .ssh</pre>
<p>Generate key pairs</p>
<pre>ssh-keygen</pre>
<p>Open the content of the public key</p>
<pre>cat id_rsa.pub</pre>
<p>Copy and paste the public key in its entirety to GCP and save</p>
<img src="img/Picture4.png" width=600/>
<img src="img/Picture5.png" width=600/>
<br>
<p>Get the external IP address</p>
<img src="img/Picture6.png" width=600/>
<p>In the local computer terminal, in the .ssh folder, enter</p>
<pre>ssh {username}@{external ip address}</pre>

## 3. Run Streamlit app on the VM
<p>Get the github repo address</p>
<img src="img/Picture7.png" width=600/>
<p>In the local computer terminal, clone the repo</p>
<pre>git clone {git repo address}</pre>
<p>Update apt</p>
<pre>sudo apt update</pre>
<p>Install virtualenv</p>
<pre>sudo apt install virtualenv</pre>
<p>Create a virtual environment</p>
<pre>virtualenv --python=python3 venv</pre>
<p>Activate the virtual environment</p>
<pre>source venv/bin/activate</pre>
<p>Install required packages</p>
<pre>pip install –r requirements.txt</pre>
<p>Then run the app</p>
<pre>streamlit run st-app.py</pre>

## 4.

