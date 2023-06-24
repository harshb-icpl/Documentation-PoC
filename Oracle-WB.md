<!DOCTYPE html>
<html>

<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Oracle-WB</title>
  <link rel="stylesheet" href="https://stackedit.io/style.css" />
</head>

<body class="stackedit">
  <div class="stackedit__left">
    <div class="stackedit__toc">
      
<ul>
<li><a href="#oracle-weblogic-server-setup">Oracle Weblogic Server Setup</a>
<ul>
<li><a href="#installation">Installation</a></li>
<li><a href="#configure-openssh-for-windows">Configure OpenSSH for Windows:</a></li>
<li><a href="#setting-path-for-java_home-jdk-and-openssh">Setting path for JAVA_HOME, JDK and OpenSSH</a></li>
<li><a href="#installing-oracle-weblogic-generic-server">Installing Oracle Weblogic Generic Server</a></li>
<li><a href="#setup-configuration-for-admin-user">Setup Configuration for Admin user</a></li>
<li><a href="#access-oracle-weblogic-generic-server">Access Oracle Weblogic Generic Server</a></li>
</ul>
</li>
</ul>

    </div>
  </div>
  <div class="stackedit__right">
    <div class="stackedit__html">
      <h1 id="oracle-weblogic-server-setup">Oracle Weblogic Server Setup</h1>
<h2 id="installation">Installation</h2>
<h3 id="java">Java:</h3>
<ul>
<li>
<p>To install Java for windows, refer to the below link:</p>
<ul>
<li><a href="https://www.java.com/en/download/manual.jsp">Download from here</a> (offline-mode is preferable)</li>
</ul>
</li>
<li>
<p>Follow the installation steps and install Java.</p>
</li>
</ul>
<p><b>Check the version of Java installed:</b></p>
<ul>
<li>Open Command prompt (cmd.exe) and execute the command <code>java -version</code>.</li>
</ul>
<img src="https://i.ibb.co/zFgDhzm/version-check.png" alt="version-check" border="0">
<h3 id="java-jdk-v1.8.0_191">Java JDK v1.8.0_191:</h3>
<blockquote>
<p><b>NOTE:</b> For Oracle Weblogic Server Generic version, JDK version should be v1.8.0_191 as it is mentioned during installation process.</p>
</blockquote>
<ul>
<li>
<p>To download mentioned JDK version for Generic installer, download it from <a href="https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html">here.</a></p>
</li>
<li>
<p>Follow instructions to install JDK.</p>
</li>
<li>
<p>To verify installation, navigate to Setting -&gt; Apps and check the version.<br>
<img src="https://i.ibb.co/QCxy4yc/jdk-version.png" alt="jdk-version" border="0"></p>
</li>
</ul>
<h2 id="configure-openssh-for-windows">Configure OpenSSH for Windows:</h2>
<p>To configure OpenSSH on windows please check the attached blog link.<br>
<a href="https://adamtheautomator.com/openssh-windows/">https://adamtheautomator.com/openssh-windows/</a></p>
<h2 id="setting-path-for-java_home-jdk-and-openssh">Setting path for JAVA_HOME, JDK and OpenSSH</h2>
<ul>
<li>Check the location where JDK is installed. By default it is under <code>(C:\ProgramFiles\Java\jdk1.8.0_191)</code></li>
</ul>
<img src="https://i.ibb.co/1bPynPB/java-home-path.png" alt="java-home-path" border="0">
<ul>
<li>
<p>Now for the environment path of <code>JAVA_HOME</code>, <code>JDK_HOME</code> and <code>OpenSSH</code>, open <strong>Environment Variables for your account</strong> window.</p>
<ul>
<li>Add the path as mention below:</li>
</ul>
</li>
</ul>
<img src="https://i.ibb.co/1vhzJty/all-paths.png" alt="all-paths" border="0">
<ul>
<li>Also please check this link for setting environment path:<br>
<a href="https://stackoverflow.com/questions/1672281/how-to-set-the-environment-variables-for-java-in-windows">https://stackoverflow.com/questions/1672281/how-to-set-the-environment-variables-for-java-in-windows</a></li>
</ul>
<h2 id="installing-oracle-weblogic-generic-server">Installing Oracle Weblogic Generic Server</h2>
<ul>
<li>
<p>To install  Generic Server visit the attached below link and also unzip the installed zip file.<br>
<a href="https://www.oracle.com/in/middleware/technologies/weblogic-server-downloads.html">https://www.oracle.com/in/middleware/technologies/weblogic-server-downloads.html</a></p>
</li>
<li>
<p>Run command prompt as Administrator and navigate the folder where the extract <code>.jar</code> file is present.</p>
</li>
</ul>
<img src="https://i.ibb.co/qdYq1ML/jar-file-location.png" alt="jar-file-location" border="0">
<ul>
<li>Execute the command <code>java -jar file-name.jar</code> and hit enter.</li>
</ul>
<img src="https://i.ibb.co/vQQGqRv/installation.png" alt="installation" border="0">
<ul>
<li>
<p>This will start Weblogic Server installation.</p>
</li>
<li>
<p>Follow the instructions and complete the install setup.</p>
</li>
</ul>
<h2 id="setup-configuration-for-admin-user">Setup Configuration for Admin user</h2>
<ul>
<li>After successful installation of Weblogic Server, Configuration Panel will open.</li>
</ul>
<blockquote>
<p><strong>NOTE:</strong> Initially for the first time after installation, configuration panel will be by default for Admin user.</p>
</blockquote>
<ul>
<li>
<p>You can also manually run configuration wizard for Weblogic server.</p>
<ol>
<li>Open <code>cmd</code> as Administrator and navigate to <code>C:\Oracle\Middleware\Oracle_Home\oracle_common\common\bin</code> (by default path, if not then enter your saved path)</li>
<li>Execute the command <code>config.cmd</code>.</li>
</ol>
  <img src="https://i.ibb.co/LCmH0R1/config.png" alt="config" border="0">
<ol start="3">
<li>Follow the instructions and user will be created.</li>
</ol>
</li>
</ul>
<blockquote>
<p><strong>NOTE:</strong> Make sure to change the <strong>servername</strong> from <strong>localhost</strong> to <strong>local-network</strong> to access inside LAN network or <strong>0.0.0.0</strong> for remote-user as per your preference.</p>
</blockquote>
<h2 id="access-oracle-weblogic-generic-server">Access Oracle Weblogic Generic Server</h2>
<p>To use the Weblogic Server, open the following link on the browser:</p>
<p><a href="http://172.17.16.63:7001/console">http://172.17.16.63:7001/console</a></p>

    </div>
  </div>
</body>

</html>
