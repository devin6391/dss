# Define scopes

## Creation
* create_resource
* create_info
* create_remote
* create_tags
* create_media
* create_user
* create_role
* create_authprovider
* create_interaction
* create_initiative
* create_scope

## Updation
* update_resource
* update_info
* update_remote
* update_tags
* update_media
* update_user
* update_role
* update_authprovider
* update_interaction
* update_initiative
* update_scope

## Delete
* delete_resource
* delete_info
* delete_remote
* delete_tags
* delete_media
* delete_user
* delete_role
* delete_authprovider
* delete_interaction
* delete_initiative
* delete_scope

## Read
* read_resource
* read_info
* read_remote
* read_tags
* read_media
* read_user
* read_role
* read_authprovider
* read_interaction
* read_initiative
* read_scope

# Others
* broadcast_social
* update_ui_layout

# Define User roles

## Admin
> Admin needs to log in the app. Tech admin must setup admin.

* create_resource
* create_info
* create_tags
* create_media
* create_interaction
* create_initiative
* update_resource
* update_info
* update_media
* update_user
* update_interaction
* update_initiative
* delete_resource
* delete_info
* delete_media
* delete_interaction
* delete_initiative
* read_resource
* read_info
* read_remote
* read_tags
* read_media
* read_user
* read_role
* read_authprovider
* read_interaction
* read_initiative
* read_scope
* broadcast_social
* update_ui_layout

## Super user
> Access db, code, etc.

* create_resource
* create_info
* create_remote
* create_tags
* create_media
* create_user
* create_role
* create_authprovider
* create_interaction
* create_initiative
* create_scope
* update_resource
* update_info
* update_remote
* update_media
* update_user
* update_role
* update_interaction
* update_initiative
* delete_resource
* delete_info
* delete_remote
* delete_tags
* delete_media
* delete_user
* delete_role
* delete_authprovider
* delete_interaction
* delete_initiative
* delete_scope
* read_resource
* read_info
* read_remote
* read_tags
* read_media
* read_user
* read_role
* read_authprovider
* read_interaction
* read_initiative
* read_scope

## User
> A user that needs to log in

* read_resource
* read_info
* read_remote
* read_media
* read_authprovider
* read_interaction
* read_initiative
* create_interaction
* update_interaction

## Guest user
> Any general viewer

* read_resource
* read_info
* read_remote
* read_media
* read_authprovider
* read_interaction
* read_initiative


# Create Users for Admin, SU and guest

# Auth system for DSS to generate tokens which would encapsulate scopes or roles.

# Integrate auth platforms and create a login system for admin
* Use of fb, google, youtube, wikipedia, photos etc. for admin account.
* Create admin page to login into DSS, and then to auth providers.

# Admin should be able to create stuffs while guest should be able to view them