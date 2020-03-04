# Private Blockchain for the Stars

## Purpose

This is a private blockchain that allows users to register a star to their bitcoin wallet!

## Notes

Although we are asked not to modify the file `BlockchainController.js`, I had to make some changes in order to meet the project requirements.
We are asked to create endpoints to retrieve a block based on height and on hash. The original file contains the same endpoint for both these,
`/block/:height` and `/block/:hash`. There is no way to distinguish between the two. I modified the file, starting at line 28, so that the code
looks for how long the parameter is. If it's equal to 64 characters, then the code assumes that it is a hash being passed in, not a height.

Second, there is no endpoing to test for chain validation. Therefore, I added another endpoint, starting at line 133. It allows the user to
validate the entire chain by posting to `/validate`.
