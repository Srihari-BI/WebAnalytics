# WebAnalytics

Schema

Visitors
visitor_id (INT, Primary Key)
ip_address (VARCHAR)
country (VARCHAR)
city (VARCHAR)
browser (VARCHAR)
operating_system (VARCHAR)
device_type (VARCHAR)
first_visit_timestamp (TIMESTAMP)
last_visit_timestamp (TIMESTAMP)

Pageviews
pageview_id (INT, Primary Key)
visitor_id (INT, Foreign Key to Visitors)
page_url (VARCHAR)
page_title (VARCHAR)
page_type (VARCHAR)
visit_timestamp (TIMESTAMP)
time_spent_seconds (INT)
referring_url (VARCHAR)
device_type (VARCHAR)

Events
event_id (INT, Primary Key)
visitor_id (INT, Foreign Key to Visitors)
event_name (VARCHAR)
event_category (VARCHAR)
event_label (VARCHAR)
event_value (INT)
event_timestamp (TIMESTAMP)
page_url (VARCHAR)
device_type (VARCHAR)

Conversions
conversion_id (INT, Primary Key)
visitor_id (INT, Foreign Key to Visitors)
conversion_goal (VARCHAR)
conversion_timestamp (TIMESTAMP)
conversion_value (DECIMAL)
conversion_type (VARCHAR)
conversion_details (TEXT)
