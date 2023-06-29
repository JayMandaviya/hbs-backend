# Hotel Booking System

## Server Configuration

First of all, don't forget to configure your **database** (look into the resource folder the schema), the sql file was generated to use MySQL or MariaDB.

### Installing Dependencies

```bash
$ npm install
```

### Setting up

Inside src/config there's configuration environment variables, setup your database here.

### Running

To start the project, just run on your console
```bash
$ npm start
```

In case you need to debug, you can use chrome debugger through inspect plugin (don't forget to enabled using chrome://inspect once that you have ran the server)
```bash
$ npm run inspect
```

### Generate cert key files

Execute the next command

```bash
openssl genrsa -out server.key 2048
openssl rsa -in server.key -out server.pem -outform PEM -pubout
```

Once you have the keys, move the generated files into keys/ folder or whatever you want, just don't forget to configure the right path into src/config/{development | production}.config.json



**Making requests**

All api endpoints are secure and you will need the token to call them, so once you get a token after login, in every request you need to send the token using the "Authorization" header with the value "BEARER {token}".

