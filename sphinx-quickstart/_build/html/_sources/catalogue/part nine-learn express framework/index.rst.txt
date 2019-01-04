Part nine: learn express web framework
=========================================
Express.js, or simply Express, is a web application framework for Node.js, 
released as free and open-source software under the MIT License. 
It is designed for building web applications and APIs.
It has been called the de facto standard server framework for Node.js.

=================
installation
=================
.. code-block:: shell

    npm install express -g
    npm install express-generator -g



===============
Quickly start
===============
.. code-block:: shell

    mkdir myapp
    cd myapp
    npm init
    entry point: (index.js)
    npm install express --save
    express --view=pug myfirstweb
    cd myfirstweb
    npm install
    DEBUG=myfirstweb:* npm start or node ./bin/www

Once it’s running, open a browser to http://localhost:3000/.

`More details see official website`__

.. __: https://expressjs.com/

