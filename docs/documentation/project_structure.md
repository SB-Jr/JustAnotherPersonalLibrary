# Folder and File structure

The prject has been devided into 2 components

1. Interface
2. Engine



## Interface

User interface will contain the code which interacts with the user only. 

Currently the sub-components in UI are:

1. Document interface
2. Dashboard
3. Search Interface 
4. Folder View interface
5. Onboarding interface
6. Configuration Interface
7. Pluggin Marketplace



# Engine

The bakend will contain all the logic and file handling code.

Currently the sub-components of Backend are:

1. Indexing Engine
2. JavaScript Wrapper 
3. Search engine wrapper
4. Dasboard engine
5. Document engine
6. Configuration engine
7. Pluggin engine
8. CLI 



# Detailed Explanation

## Interface

### Document Iterface

1. _Fetch Document Layer_: Fetches the document user wants to view.
2. _Config Transformer_: Transforms the fetched document according to the user’s configuration
3. _Document Display Interface_: Displays the document onto a view for user’s viewing
4. _In Document Search_: Provide search interface while displaying document. Seacrh can be either local(i.e. in current document) or global(i.e. in the whole file system using engine)

### Dashboard

1. _Fetch Dashboard_: Fetches dashboard data for the user.
2. _Config Transformer_: Transforms the fetched dashboard according to the user’s configuration
3. _Dashboard Display Interface_: Displays the trasnformed dashboard data for user’s viewing

### Search Interface

1. _Show Search Box_: Dispays a search box and other options according to the user’s configuration
2. _Post Search Query_: Posts the search query to the engine
3. _Fetch Search Query_: Fetches the query results from engine
4. _Config Transformer_: Transforms the result as per user’s configuration
5. _Display Result_: Display the transformed result to the user.
6. _Open File_: Posts the file info for fetching file data selected by user

### Folder View Interface

1. _Fetch Folders_: Fetches the list of files and folders.
2. _Config Transformer_: Trasnforms the fetched result as per user’s configuration
3. _Display Result_: Shows the result to the user after it is trasnformed
4. _Open File_: Post file info to open a file requested by user

### OnBoarding Interface

1. Show animations and button highlighter
2. Tips and Tricks Highlighter

### Configuation Interface

1. _Configuration Fetch_: Fetched stored configuration
2. _Configuration Change Interface_: Allowing user to change different configuration
3. _Configuration store_: Posting configuration to engine for stpring purpose
4. _Configuration Change Effect_: Reloading interface configuration if any interface related configuration has changed

### Plugin MarketPlace

1. _Store for Plugin_: Showing different plugin available for download
2. _Plugin Manager_: Showing plugins already downloaded and actions to perform on them
3. _Plugin Instal_: Posting a plugin install query
4. _Plugin Remove_: Posting a plugin remove query
5. _Config Update_: Updating config on plugin install/remove