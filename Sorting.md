????????????????????????

非對稱加密

How would you add authentication to an API?
HTTP Basic Auth: HTTP Basic Authentication is rarely recommended due to its inherent security vulnerabilities
API Keys: API keys are widely used in the industry and became some sort of standard, however, this method should not be considered a good security measure
OAuth 2.0: OAuth 2.0 is the best choice for identifying personal user accounts and granting proper permissions. This is fundamentally a much more secure and powerful system than the other approaches.

How would you store a password?
Store the password after adding salt (random bit of data added to the password ) and encrypt with SHA1 or Bcrypt  

Concurrency : Concurrency is run multiple tasks not exactly at the same time, but running the all things at once.

Parallelism : Parallelism is all the tasks run at the same time


--
Styled components :
1. Easy to export
2. Easy to pass the props to control the state

1. Need to write the components before actually use, not intuition

SCSS/CSS :
1. Easy to write

1. Not semantic
2. Hard to control state
3. The structure sometimes become complicate, use plugins such as react icons which are components, 
use SCSS/CSS with Styled components
