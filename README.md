# Django Blog

## Step by step project setup

### Project User Story on Github

#### User Stories
    - View post list: As a **Site User** I can **view a paginated list of posts** so that I can select one to read
    - Open a post: As a **Site User** I can **click on a post** so that **I can read the full text**
    - View likes: As a **Site User / Admin** I can **view the number of likes on each post** so that **I can see which is the most popular or viral**
    - View comments: As a **Site User / Admin** I can **view comments on an individual post** so that **I can read the conversation**
    - Account registration: As a **Site User** I can **register an account** so that **I can comment and like**
    - Comment on a post: As a **Site User** I can **leave comments on a post** so that **I can be involved in the conversation**
    - Like / Unlike: As a **Site User** I can **like or unlike a post** so that **I can interact with the content**
    - Manage posts: As a **Site Admin** I can **create, read, update and delete posts** so that **I can manage my blog content**
    - Create drafts: As a **Site Admin** I can **create draft posts** so that **I can finish writing the content later**
    - Approve comments: As a **Site Admin** I can **approve or disapprove comments** so that **I can filter out objectionable comments**

#### User Stories Project creation

1. Use github `Setup`->`Features`->`Issues`->`Setup Templates` button to create the `User Story` custom template as default user story template. 
    - Template name: "`User Story`"
    - About:  "`Default user story`"
    - Template Content: "`As a **role** I can **capability** so that **received benefit**`"
    - Issue default title: "`USER STORY: <TITLE>`"
  
2. Use github `Projects` menu option to create a new project named `Django Blob User Stories` with  `Board` template.
3. From the project `To Do` list add `Isues` using the new `User Story` template to create all the the User Story items.

#### Setting up de development environment under CodeAnywhere

1. Install Django
    > For this project we have choosen django version 3
    ```cli
    pip3 install 'django<4'
    ```
2. Install Django supporting libraries
   ```cli
   pip3 install gunicorn
   pip3 install dj_database_url==0.5.0      # PosgreSQL support libraries
   pip3 install psycopg2                    # PosgreSQL connection libraries
   pip3 install dj3-cloudinary-storage      # Cloudinary Support libraries 
   pip3 install urllib3==1.26.15
   ```
3. Create a new, blank Django project
    > (Don’t forget the . )
   ```cli
    django-admin startproject codestar .
    ```
4. Create a new Django app
    - Create the new Django application
        ```cli
        python3 manage.py startapp blog
        ```
   - Add '`blog,`' to the list `INSTALLED_APPS` in file `codestar/settings.py`
   - Migrate changes to the database 
        ```cli
        python3 manage.py migrate
        ```
5. Test Django setup
   - Start the server
    >This first run may not work because the host is not authorized
        ```cli
        python3 manage.py runserver
        ```
   - If there was a DisallowedHost error, add the host to the list `ALLOWED_HOSTS` in file `codestar/settings.py`

6. Create new external database
    > We will use ElephantSQL as a database provider
   1. Create/log in your ElephantSQL account (if you don't have one already)
       - Navigate to ElephantSQL.com and click `Get a managed database today`
       - Select `Try now for FREE` in the TINY TURTLE database plan
       - Select `Log in with GitHub` and authorize ElephantSQL with your selected GitHub account
       - In the Create new team form:
           - Add a team name (your own name is fine)
           - Read and agree to the Terms of Service
           - Select Yes for GDPR
           - Provide your email address
           - Click “Create Team”
           - Your account is supossed to be successfully created
   2. Create New service Instance
       - Setup your plan name (this is commonly the name of the project)
       - Select your plan type ( use the Free plan)
       - Select the region closest to your location (E.g. azure westeurope)
       - confirm the instance creation
   3. Select the new database instance from the dashboard and copy the database URL for later 
    (e.g. `postgres://napnlvrl:REyrb2FxoDbJjXblSVvGmL1XQrGu8lbN@dumbo.db.elephantsql.com/napnlvrl`)
    
1. Deploy the empty app to Heroku
   1. Create the _Heroku app
   
2. Set our project to use Cloudinary
3. Set our project to use PostgreSQL
4. Deploy a new, empty project to Heroku

 
### Setup Heroku 
You can now use the `heroku` CLI program - try running `heroku apps` to confirm it works. This API key is unique and private to you so do not share it. If you accidentally make it public then you can create a new one with _Regenerate API Key_.

---

Happy coding!
