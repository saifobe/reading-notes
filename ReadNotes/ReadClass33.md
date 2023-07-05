# Authentication & Production Server

## Why is authentication important?
- Authentication is important because it allows us to know who is accessing our application. It is the process of verifying the identity of a user or process. Authentication is commonly performed by submitting a username or ID and one or more items of private information that only a given user should know.

## Why should we be careful about storing a user’s password?
- We should be careful about storing a user's password because if someone gets a hold of the password, they can access the user's account and do whatever they want with it. It is important to store passwords securely

## What is the difference between hashing and encryption?
- Hashing is a one way function that cannot be reversed. Encryption is a two way function that can be reversed.

## What is the difference between encryption and encoding?
- Encoding is for maintaining data usability and can be reversed by employing the same algorithm that encoded the content, i.e. no key is used. Encryption is for maintaining data confidentiality and requires the use of a key (kept secret) in order to return to plaintext.

## What is a token used for?
- A token is used to authenticate a user. It is a unique string of characters that is used to verify the user's identity.

## What is a bearer token?
- A bearer token is a security token that is issued to the client. It is used to access protected resources.

## Why do we use bearer token?
- We use bearer tokens because they are easy to implement and they are stateless. They are also easy to revoke.

## Document the following Vocabulary Terms
- **encryption** - Encryption is the process of converting data to an unrecognizable or "encrypted" form. It is commonly used to protect sensitive information so that only authorized parties can view it.

- **token** - A token is a unique string of characters that is used to verify the user's identity.

- **bearer** - A bearer token is a security token that is issued to the client. It is used to access protected resources.

- **secret** - A secret is a piece of information that is only known by the user and the server. It is used to verify the user's identity.

- **JSON Web Token** - A JSON Web Token is a JSON object that is used to securely transfer information between two parties. It is digitally signed and can be verified.


