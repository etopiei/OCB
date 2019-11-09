# OCB

A repo containing sub-modules which together make up the code for the open chess browser

To get started recursively clone:

	$ git clone --recurse-submodules git@github.com:etopiei/OCB.git

This will clone all the parts of this project to a local folder called OCB.

## Development

There are a few necessary dependencies:

 - python3
 - neo4j server
 - rust + cargo
 - wasm-pack

Then to get going:

1. Import PGN file(s) into the neo4j server with 'dbbuilder' (more detailed instructions will be in that repo) This will act as the game database.

2. Open a new terminal and start the 'chessgraphserver' (instructions included in that repo) This will take requests from the front-end and process them and return results from the neo4j database.

3. Build the front-end WASM in 'openchessbrowser' with:

	$ wasm-pack build

4. Run the frontend from 'openchessbrowser' with:

	$ cd www
	$ npm run start
