# Task Manager App

# User
has_many :tasks
has_many :comments
has_many :task_lists, through: tasks
- First Name
- Last Name
- Email
- Password_digest

# Task List
has_many :tasks
has_many :users, through: tasks
has_many comments, through: tasks
- Title
- Tasks?

# Task
belongs_to :task_list
belongs_to :user
has_many :comments
- Title
- Content
- Status
- Comments

# Comments
belongs_to :user
belongs_to :task
- Name
- Content


[ ] - Include 1 has_many, 1 belongs_to, 2 has_many :through AND the join table must include a suer-submittable attribute
[ ] - Models must include reasonable validations (Support against invalid data)
[ ] - One class level ActiveRecord Scope Method -> Must be chainable -> Must use an ActiveRecord Query Method within it
[ ] - Standard User Authentication
[ ] - Allow for 3rd party login (GitHub)
[ ] - Nested Routes -> Nested `new` directly related to parent AND nested `index` or `show`
[ ] - Correctly display validation errors in forms
[ ] - Application should be DRY


**BUGS**
- Fix the new user not adding username