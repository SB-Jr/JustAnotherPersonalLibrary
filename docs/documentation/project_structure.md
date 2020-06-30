# Folder and File structure

The prject has been devided into 2 components

1. Interface
2. Engine
3. CLI tool



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
8. Interface Controller
9. Interface Model



## Engine

The bakend will contain all the logic and file handling code.

Currently the sub-components of Backend are:

1. Indexing Engine
2. Engine Wrapper 
3. Search engine wrapper
4. Dasboard engine
5. Document engine
6. Configuration engine
7. Pluggin engine



## CLI tool

Cli tool will provide a fast interface to the engine with least focus on customization and gui.

1. Search Interface
2. Folder/File Interface
3. CLI Plugin interface



# Detailed Explanation

## Interface

### Document Iterface

1. _Fetch Document Layer_: Fetches the document user wants to view.
2. _Config Transformer_: Transforms the fetched document according to the user’s configuration
3. _Document Display Interface_: Displays the document onto a view for user’s viewing
4. _In Document Search_: Provide search interface while displaying document. Seacrh can be either local(i.e. in current document) or global(i.e. in the whole file system using engine)
5. _Generate Metdata_: Generate metadata based on some policy and post the metadata to engine

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
7. _Generate Metadata_: create metadata based on some policy and post the metadata to engine

### Folder View Interface

1. _Fetch Folders_: Fetches the list of files and folders.
2. _Config Transformer_: Trasnforms the fetched result as per user’s configuration
3. _Display Result_: Shows the result to the user after it is trasnformed
4. _Open File_: Post file info to open a file requested by user
5. _Generate Metadata_: create metadata based on some policy and post the metadata to engine

### OnBoarding Interface

1. _Initial Configuration_: Setup initial configuration for user
2. Show animations and button highlighter
3. Tips and Tricks Highlighter
4. _Generate Metadata_: create metadata based on some policy and post the metadata to engine

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

### Interface Controller

1. Format post calls with proper header and body
2. Parse request-reply for User interface parsing

### Interface Model

1. Store cache if required
2. Store view configurations



## Engine

### Indexing Engine

1. _Initial Index_: Create initial index of all the files added during onboarding
2. _New Index_: Re-create index on addition of new files or folder
3. _Fetch Index_: fetch index on search query

### Interface Wrapper

1. _Provide Search functionality_
2. _Provide dashboard functionality_
   1. _Create_
   2. _Update_
   3. _Retrieve_
3. _Provide File/Folder reading functionality_
4. _Provide Metadata functionality_
   1. _Create_
   2. _Update_
   3. _Retreive_
5. _Plugin Functionality_
   1. _Update_
   2. _Install_
   3. _Remove_
6. _Configuration Functionality_
   1. _Create_
   2. _Update_
   3. _Retrieve_

### Search Engine Wrapper

1. _Query Generator_: generate query based on search input
2. _Result Formater_: format the results provided by search engine for cli or user interface 

### DashBoard Engine

1. _Create Dashboard_: generate the dashboard on user onboarding
2. _Retreive Dashboard_: retreive the dashboard when querried
3. _Metadata Handling_: Update dashboard on metadata create/update/retreive
4. _Augment Search_: update/change search result based on metadata entries

### Document Engine

1. _Retrieve Document_: read and provide docuement query
2. _Retrieve Folders_: read folder and file structure and provide result on query