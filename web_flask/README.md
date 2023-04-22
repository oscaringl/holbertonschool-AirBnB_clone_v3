<h2 dir="auto">Web Framework</h2>
<blockquote>
<p dir="auto">In the backend, we use Flask as the web framework and Jinja as the template.</p>
</blockquote>
<h3 dir="auto"><a id="user-content-resources" class="anchor" href="https://github.com/MelissaN/AirBnB_clone_v2#resources" aria-hidden="true"></a>Resources:</h3>
<ul dir="auto">
<li><a href="https://jeffknupp.com/blog/2014/03/03/what-is-a-web-framework/" rel="nofollow">What is a web framework?</a></li>
<li><a href="http://flask.pocoo.org/docs/1.0/quickstart/" rel="nofollow">Flask - Quickstart: Minimal Application, Routing except HTTP methods, Rendering templates</a></li>
<li><a href="http://jinja.pocoo.org/docs/2.9/templates/" rel="nofollow">Jinja - Template Designer: Synopsis, Variables, Comments, Whitespace control, List of Control Structures (read up to Call)</a></li>
</ul>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto">
<pre class="notranslate"><code># import data on cities and states into sql database
$ curl -o 7-dump.sql "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/290/7-states_list.sql"
$ cat 7-dump.sql | mysql -uroot -p
Enter password: 
$ HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db python3 -m web_flask.8-cities_by_states
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....
</code></pre>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto">
<pre class="notranslate"><code># import data on places into sql database
$ curl -o 10-dump.sql "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/290/10-hbnb_filters.sql"
$ cat 10-dump.sql | mysql -uroot -p
Enter password: 
$ HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db python3 -m web_flask.10-hbnb_filters
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....
</code></pre>
<div class="snippet-clipboard-content notranslate position-relative overflow-auto">
<pre class="notranslate"><code># test flask web app displays

# add this line into Vagrantfile on host
config.vm.network :forwarded_port, guest: 5000, host: 5000

# vagrant reload

# open connection
$ HBNB_MYSQL_USER=hbnb_dev HBNB_MYSQL_PWD=hbnb_dev_pwd HBNB_MYSQL_HOST=localhost HBNB_MYSQL_DB=hbnb_dev_db HBNB_TYPE_STORAGE=db python3 -m web_flask.10-hbnb_filters
* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
....

# check in browser
0.0.0.0:5000/hbnb or 127.0.0.1:5000/hbnb

# or check in CLI
curl 0.0.0.0:5000/hbnb ; echo ""
</code></pre>
<h3 dir="auto"><a id="user-content-description-of-what-each-file-shows" class="anchor" href="https://github.com/MelissaN/AirBnB_clone_v2#description-of-what-each-file-shows" aria-hidden="true"></a>Description of what each file shows:</h3>
<ul dir="auto">
<li>File 100-hbnb.py and templates/100-hbnb.html is cummulative of all files. The simple web-app shows how to use Flask to map what we see at each route, which html pages, and how to customize the html templates using Jinja. Each file can be run with <code>python -m [dirname].[filename]</code>. This results in <code>* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)</code>. To test the web app is running, for instance, in another terminal we can run <code>curl 0.0.0.0:5000/number_odd_or_even/89 ; echo ""</code> and should see the return value of our routes.</li>
</ul>
<h3 dir="auto"><a id="user-content-environment" class="anchor" href="https://github.com/MelissaN/AirBnB_clone_v2#environment" aria-hidden="true"></a>Environment</h3>
<ul dir="auto">
<li>Languages: Python 3.4.3, HTML, CSS</li>
<li>OS: Ubuntu 14.04 LTS</li>
<li>Framework: Flask <code>pip3 install flask</code></li>
<li>Style guidelines: <a href="https://github.com/holbertonschool/W3C-Validator">W3C-Validator</a> || <a href="https://www.python.org/dev/peps/pep-0008/" rel="nofollow">PEP 8 (version 1.7) for Python 3.5</a> || <a href="http://sphinxcontrib-napoleon.readthedocs.io/en/latest/example_google.html" rel="nofollow">Google Style Python Docstrings</a></li>
</ul>
<hr />
<h3 dir="auto"><a id="user-content-authors" class="anchor" href="https://github.com/MelissaN/AirBnB_clone_v2#authors" aria-hidden="true"></a>Authors</h3>
<p dir="auto">Oscar Guerra</p>
</div>
</div>
</div>