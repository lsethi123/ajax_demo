### Ajax Demao


To show the Current time on the index page

Added code in  index.html.erb

<div id="datePanel">
  The Current Time is <span id=time_span> <%= @current_time%></span>
  <span> <%=link_to 'Update Time',posts_update_time_path, :remote=>true%></span>
</div>

set action as remote:true to call the update_time function using ajax get method

create action called update_time in Posts controller which return you the current time and its response is .js

Create the update_time.js.erb which will update the time_span content run time using the ajax

Added action in routes

get "posts/update_time"

steps to run app

1)change the database.yml file
2)rake db:create
3)rake db:migrate
4)rails s
