# mysql-shell-plugin-demo
This demo plugin shows how to extend the MySQL Shell with extension objects. 

It will register a new MySQL Shell global object called "ext" and add an extension object called 'demo' with two functions,  hello_world() and show_schemas(). 

After installing the demo into the plugins directory of the MySQL Shell, the plugin can be accessed like this.

```
MySQL JS> \? ext.demo
NAME
      demo - Demo object to showcase MySQL Shell Plugins.

DESCRIPTION
      Demo object to showcase MySQL Shell Plugins.

FUNCTIONS
      helloWorld()
            Prints Hello world!.

      help([member])
            Provides help about this object and it's members
      
      showSchemas([session])
            Lists all database schemas.

MySQL JS> ext.demo.helloWorld()
Hello world!

MySQL JS> \py
Switching to Python mode...

MySQL PY> ext.demo.hello_world()
Hello world!
```

## Installation
To install this demo on your machine type the following commands after you have installed the MySQL Shell and the git command line tools.

This will clone the repository and copy the files to the right path in order to be automatically loaded on MySQL Shell startup.

### macOS / Linux
```
$ mkdir -p ~/.mysqlsh/plugins
$ git clone https://github.com/mzinner/mysql-shell-plugin-demo.git ~/.mysqlsh/plugins/demo
```

### Windows
```
$ mkdir %AppData%MySQL\mysqlsh\plugins
$ git clone https://github.com/mzinner/mysql-shell-plugin-demo.git %AppData%MySQL\mysqlsh\plugins\demo
```

## Extending the MySQL Shell

Please take a look at the init.py file to learn how to extend the MySQL Shell with plugins.

