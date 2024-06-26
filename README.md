Options -Indexes

<IfModule mod_rewrite.c>
	RewriteEngine On
	
	RewriteRule ^index$ index.php
	RewriteRule ^sitemap.xml$ sitemap.php
 	RewriteRule ^login$ index.php?page=login 
	RewriteRule ^logout$ index.php?page=logout 
	RewriteRule ^register$ index.php?page=register 
	RewriteRule ^resend-activation$ index.php?page=resendactivation 
	RewriteRule ^submit$ index.php?page=submit
	RewriteRule ^lost-password$ index.php?page=lostpassword 
	RewriteRule ^reset-password/(.*)/(.*)$ index.php?page=resetpassword&email=$1&lost_password_code=$2 
	RewriteRule ^activate/(.*)/(.*)$ index.php?page=activate&email=$1&activation_code=$2
	RewriteRule ^not-found$ index.php?page=notfound
	RewriteRule ^purchase-highlight$ index.php?page=purchase_highlight

	RewriteRule ^terms-of-service$ index.php?page=tos
	RewriteRule ^contact$ index.php?page=contact
	RewriteRule ^privacy-policy$ index.php?page=privacy_policy
	RewriteRule ^disclaimer$ index.php?page=disclaimer

	RewriteRule ^settings/design$ index.php?page=designs 
	RewriteRule ^settings/password$ index.php?page=password 
	RewriteRule ^settings/profile$ index.php?page=settings 

	RewriteRule ^edit-server/(.*)/(.*)/(.*)$ index.php?page=server_edit&server_id=$1&type=$2&token=$3
	RewriteRule ^edit-server/(.*)$ index.php?page=server_edit&server_id=$1

	RewriteRule /status/access$ index.php?status=access 
	RewriteRule ^status/loggedout$ index.php?status=loggedout 
	RewriteRule ^status/loggedin$ index.php?status=loggedin 

	RewriteRule ^admin/categories-management$ index.php?page=admin_categories_management 
	RewriteRule ^admin/categories-management/delete/(.*)/(.*)$ index.php?page=admin_categories_management&delete=$1&token=$2 
	RewriteRule ^admin/edit-category/(.*)$ index.php?page=admin_category_edit&category_id=$1 

	RewriteRule ^admin/users-management$ index.php?page=admin_users_management 
	RewriteRule ^admin/users-management/status/(.*)/(.*)$ index.php?page=admin_users_management&status=$1&token=$2 
	RewriteRule ^admin/users-management/delete/(.*)/(.*)$ index.php?page=admin_users_management&delete=$1&token=$2 
	RewriteRule ^admin/edit-user/(.*)$ index.php?page=admin_user_edit&user_id=$1 

	RewriteRule ^admin/payments-management$ index.php?page=admin_payments_management
	RewriteRule ^admin/payments-management/delete/(.*)/(.*)$ index.php?page=admin_payments_management&delete=$1&token=$2

	RewriteRule ^admin/servers-management$ index.php?page=admin_servers_management 
	RewriteRule ^admin/servers-management/status/(.*)/(.*)$ index.php?page=admin_servers_management&status=$1&token=$2 
	RewriteRule ^admin/servers-management/delete/(.*)/(.*)$ index.php?page=admin_servers_management&delete=$1&token=$2 
	 
	RewriteRule ^admin/edit-server/(.*)/(.*)/(.*)$ index.php?page=admin_server_edit&server_id=$1&type=$2&token=$3
	RewriteRule ^admin/edit-server/(.*)$ index.php?page=admin_server_edit&server_id=$1

	RewriteRule ^admin/reports-management$ index.php?page=admin_reports_management 
	RewriteRule ^admin/edit-report/(.*)$ index.php?page=admin_report_edit&report_id=$1 [QSA]

	RewriteRule ^admin/website-settings$ index.php?page=admin_website_settings
	RewriteRule ^admin/website-settings/success$ index.php?page=admin_website_settings&status=success

	RewriteRule ^admin/website-statistics$ index.php?page=admin_website_statistics
	RewriteRule ^admin/reset$ index.php?page=admin_reset

	RewriteRule ^servers$ index.php?page=servers [QSA]
	RewriteRule ^servers/([^/]+)$ index.php?page=servers&current_page=$1 [QSA]
	RewriteRule ^my-servers$ index.php?page=my_servers [QSA]
	RewriteRule ^my-servers/([^/]+)$ index.php?page=my_servers&current_page=$1 [QSA]
	RewriteRule ^my-favorites$ index.php?page=my_favorites [QSA]
	RewriteRule ^my-favorites/([^/]+)$ index.php?page=my_favorites&current_page=$1 [QSA]
	RewriteRule ^profile/([^/]+)$ index.php?page=profile&username=$1 
	RewriteRule ^server/([^/]+):([^/]+)$ index.php?page=server&address=$1&port=$2 
	RewriteRule ^category/([^/]*)$ index.php?page=category&url=$1 
	RewriteRule ^category/([^/]*)/([^/]*)$ index.php?page=category&url=$1&current_page=$2 
	RewriteRule ^banner/(.*)/(.*)/(.*)/(.*)$ pages/banner.php?server_id=$1&background=$2&text_color=$3&border_color=$4 [QSA]

</IfModule>
