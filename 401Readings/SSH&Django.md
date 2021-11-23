# Configuring Django Settings

 ## Issues  :

 1- Different environments

 2- Sensitive data. 

 3- Sharing settings between team members

 4- Django settings are a Python code. 



 ## Setting Configuration

 There is no built-in universal way to configure Django settings without hardcoding them

 + settings_local.py

 ```
 ALLOWED_HOSTS = ['example.com']
DEBUG = False
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'production_db',
        'USER': 'user',
        'PASSWORD': 'password',
        'HOST': 'db.example.com',
        'PORT': '5432',
        'OPTIONS': {
            'sslmode': 'require'
        }
    }
}

 ```

 settings_local.py file:

 ```
 ALLOWED_HOSTS = ['localhost']
DEBUG = True
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'local_db',
        'HOST': '127.0.0.1',
        'PORT': '5432',
    }
}
 ```

 Pros:

Secrets not in VCS.

Cons:

settings_local.py is not in VCS, so you can lose some of your Django environment settings.

The Django settings file is a Python code, so settings_local.py can have some non-obvious logic.

You need to have settings_local.example (in VCS) to share the default configurations for developers.



+ Separate settings file for each environment

Pros:

All environments are in VCS.

It’s easy to share settings between developers.

Cons:

You need to find a way to handle secret passwords and tokens.

“Inheritance” of settings can be hard to trace and maintain.



+ Environment variables


Pros:

Configuration is separated from code.

Environment parity – you have the same code for all environments.

No inheritance in settings, and cleaner and more consistent code.

There is a theoretical grounding for using environment variables 

Cons:

You need to handle sharing default config between developers.


+ 12 Factors.

Codebase

Dependencies

Config

Backing services

Build, release, run

Processes

Port binding

Concurrency

Disposability

Dev/prod parity

Logs

Admin processes




## Django Settings: Best practices

Keep settings in environment variables.

Write default values for production configuration (excluding secret keys and tokens).

Don’t hardcode sensitive settings, and don’t put them in VCS.

Split settings into groups: Django, third-party, project.

Follow naming conventions for custom (project) settings.



## Conclusion

The Settings file is a small but very important part of any Django project. If you do it wrong, you’ll have a lot of issues during all phases of development. But if you do it right, it will be a good basis for your project that will allow it to grow and scale in the future.


Using the environment variables approach, you can easily switch from a monolith to microservice architecture, wrap your project in Docker containers, and deploy it in any VPS or Cloud hosting platform such as: Amazon, Google Cloud, or your own Kubernetes cluster.



## What is SSH


The SSH key command instructs your system that you want to open an encrypted Secure Shell Connection. {user} represents the account you want to access.

The significant advantage offered by SSH over its predecessors is the use of encryption to ensure secure transfer of information between the host and the client. Host refers to the remote server you are trying to access, while the client is the computer you are using to access the host.


## Different Encryption Techniques

+ Symmetric Encryption

Symmetric encryption is a form of encryption where a secret key


![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/symmetric-encryption-ssh-tutorial.webp)

There is usually only one key that is used, or sometimes a pair keys where one key can easily be calculated using the other key.



+ Asymmetric Encryption

 asymmetrical encryption uses two separate keys for encryption and decryption. These two keys are known as the public key and the private key.


 ![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/asymmetric-encryption.webp)


 The public key, as the name suggest is openly distributed and shared with all parties.


 The private key must remain private i.e. for the connection to be secured, no third party must ever know it.


 Unlike the general perception, asymmetrical encryption is not used to encrypt the entire SSH session. Instead, it is only used during the key exchange algorithm of symmetric encryption. 



+ Hashing

One-way-hash functions differ from the above two forms of encryption in the sense that they are never meant to be decrypted. 

![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/ssh-tutorial-hash.webp)


SSH uses hashes to verify the authenticity of messages. This is done using HMACs, or Hash-based Message Authentication Codes. This ensures that the command received is not tampered with in any way.


## How Does SSH Work with These Encryption Techniques

SSH operates on TCP port 22 by default (though this can be changed if needed). The host (server) listens on port 22 (or any other SSH assigned port) for incoming connections. It organizes the secure connection by authenticating the client and opening the correct shell environment if the verification is successful.


![](https://www.hostinger.com/tutorials/wp-content/uploads/sites/2/2017/07/ssh-client-and-server.webp)



 stages to establishing a connection:



 ### Session Encryption Negotiation

 Here is how the algorithm works at a very basic level:

Both the client and the server agree on a very large prime number, which of course does not have any factor in common. This prime number value is also known as the seed value.

Next, the two parties agree on a common encryption mechanism to generate another set of values by manipulating the seed values in a specific algorithmic manner.
 These mechanisms, also known as encryption generators, perform large operations on the seed. An example of such a generator is AES (Advanced Encryption Standard).

Both the parties independently generate another prime number. 
This is used as a secret private key for the interaction.

This newly generated private key, with the shared number and encryption algorithm (e.g. AES), is used to compute a public key which is distributed to the other computer.

The parties then use their personal private key, the other machine’s shared public key and the original prime number to create a final shared key. This key is independently computed by both computers but will create the same encryption key on both sides.

Now that both sides have a shared key, they can symmetrically encrypt the entire SSH session. The same key can be used to encrypt and decrypt messages (read: section on symmetrical encryption).

### Authenticating the User

he final stage before the user is granted access to the server is authenticating his/her credentials. For this, most SSH users use a password. The user is asked to enter the username, followed by the password. These credentials securely pass through the symmetrically encrypted tunnel, so there is no chance of them being captured by a third party.



## Conclusion

Gaining an in-depth understanding of the underlying how SSH works can help users understand the security aspects of this technology. Most people consider this process to be extremely complex and un-understandable, but it is much simpler than most people think. If you’re wondering how long it takes for a computer to calculate a hash and authenticate a user, well, it happens in less than a second

## resources

+ [ssh-tutorial-how-does-ssh-work](https://www.hostinger.com/tutorials/ssh-tutorial-how-does-ssh-work)


+ [configuring-django-settings](https://djangostars.com/blog/configuring-django-settings-best-practices/)
