# You will need a public mongo db instance which you can get for free

- https://www.mongodb.com/docs/atlas/tutorial/deploy-free-tier-cluster/

# You will need to make sure there is a folder called uploads so you can upload images

- just create a folder called uploads

# You will need to add an .env file with your credentials

- Create .env file
- Pase the following
- Replace OPEN_AI_KEY with your Open Ai Key
- Replace MONGO_DB_URL with your mongo database url


```
#=====================================================================#
#                       LibreChat Configuration                       #
#=====================================================================#
# Please refer to the reference documentation for assistance          #
# with configuring your LibreChat environment. The guide is           #
# available both online and within your local LibreChat               #
# directory:                                                          #
# Online: https://docs.librechat.ai/install/configuration/dotenv.html #
# Locally: ./docs/install/configuration/dotenv.md                     #
#=====================================================================#

#==================================================#
#               Server Configuration               #
#==================================================#

HOST=localhost
PORT=8795

MONGO_URI=MONGO_DB_URL

DOMAIN_CLIENT=http://localhost:3080
DOMAIN_SERVER=http://localhost:3080

NO_INDEX=true

#===============#
# Debug Logging #
#===============#

DEBUG_LOGGING=true
DEBUG_CONSOLE=false

#=============#
# Permissions #
#=============#

UID=1000
GID=1000

#===============#
# Configuration #
#===============#
# Use an absolute path, a relative path, or a URL

CONFIG_PATH="/alternative/path/to/librechat.yaml"

#===================================================#
#                     Endpoints                     #
#===================================================#

ENDPOINTS=openAI

PROXY=

#===================================#
# Known Endpoints - librechat.yaml  #
#===================================#
# https://docs.librechat.ai/install/configuration/ai_endpoints.html

# GROQ_API_KEY=
# MISTRAL_API_KEY=
# OPENROUTER_KEY=
# ANYSCALE_API_KEY=
# FIREWORKS_API_KEY=
# PERPLEXITY_API_KEY=
# TOGETHERAI_API_KEY=

#============#
# OpenAI     #
#============#

OPENAI_API_KEY=OPEN_AI_KEY
OPENAI_MODELS=gpt-4,gpt-4-0613,gpt-4-vision-preview,gpt-4-0125-preview,gpt-4-turbo-preview,gpt-4-1106-preview,gpt-4-turbo-2024-04-09,gpt-4o

DEBUG_OPENAI=false

# TITLE_CONVO=false
# OPENAI_TITLE_MODEL=gpt-3.5-turbo

# OPENAI_SUMMARIZE=true
# OPENAI_SUMMARY_MODEL=gpt-3.5-turbo

# OPENAI_FORCE_PROMPT=true

# OPENAI_REVERSE_PROXY=

# OPENAI_ORGANIZATION= 

#====================#
#   Assistants API   #
#====================#

ASSISTANTS_API_KEY=OPEN_AI_KEY
# ASSISTANTS_BASE_URL=
ASSISTANTS_MODELS=gpt-4,gpt-4-0314,gpt-4-32k-0314,gpt-4-0613,gpt-4-0125-preview,gpt-4-turbo-preview,gpt-4-1106-preview,gpt-4-turbo-2024-04-09,gpt-4o

#============#
# Plugins    #
#============#

PLUGIN_MODELS=gpt-4,gpt-4-turbo-preview,gpt-4-0125-preview,gpt-4-1106-preview,gpt-4-0613,gpt-4o

DEBUG_PLUGINS=true

CREDS_KEY=f34be427ebb29de8d88c107a71546019685ed8b241d8f2ed00c3df97ad2566f0
CREDS_IV=e2341419ec3dd3d19b13a1a87fafcbfb

#==================================================#
#                      Search                      #
#==================================================#

SEARCH=false

#===================================================#
#                    User System                    #
#===================================================#

#========================#
# Moderation             #
#========================#

OPENAI_MODERATION=false
OPENAI_MODERATION_API_KEY=
# OPENAI_MODERATION_REVERSE_PROXY=

BAN_VIOLATIONS=false
BAN_DURATION=1000 * 60 * 60 * 2
BAN_INTERVAL=20

LOGIN_VIOLATION_SCORE=1
REGISTRATION_VIOLATION_SCORE=1
CONCURRENT_VIOLATION_SCORE=1
MESSAGE_VIOLATION_SCORE=1
NON_BROWSER_VIOLATION_SCORE=20

LOGIN_MAX=7
LOGIN_WINDOW=5
REGISTER_MAX=5
REGISTER_WINDOW=60

LIMIT_CONCURRENT_MESSAGES=true
CONCURRENT_MESSAGE_MAX=2

LIMIT_MESSAGE_IP=true
MESSAGE_IP_MAX=40
MESSAGE_IP_WINDOW=1

LIMIT_MESSAGE_USER=false
MESSAGE_USER_MAX=40
MESSAGE_USER_WINDOW=1

ILLEGAL_MODEL_REQ_SCORE=5

#========================#
# Balance                #
#========================#

CHECK_BALANCE=false

#========================#
# Registration and Login #
#========================#

ALLOW_EMAIL_LOGIN=true
ALLOW_REGISTRATION=true
ALLOW_SOCIAL_LOGIN=false
ALLOW_SOCIAL_REGISTRATION=false

SESSION_EXPIRY=1000 * 60 * 15
REFRESH_TOKEN_EXPIRY=(1000 * 60 * 60 * 24) * 7

JWT_SECRET=16f8c0ef4a5d391b26034086c628469d3f9f497f08163ab9b40137092f2909ef
JWT_REFRESH_SECRET=eaa5191f2914e30b9387fd84e254e4ba6fc51b4654968a9b0803b456a54b8418

# Discord
DISCORD_CLIENT_ID=
DISCORD_CLIENT_SECRET=
DISCORD_CALLBACK_URL=/oauth/discord/callback

# Facebook
FACEBOOK_CLIENT_ID=
FACEBOOK_CLIENT_SECRET=
FACEBOOK_CALLBACK_URL=/oauth/facebook/callback

# GitHub
GITHUB_CLIENT_ID=
GITHUB_CLIENT_SECRET=
GITHUB_CALLBACK_URL=/oauth/github/callback

# Google
GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=
GOOGLE_CALLBACK_URL=/oauth/google/callback

# OpenID
OPENID_CLIENT_ID=
OPENID_CLIENT_SECRET=
OPENID_ISSUER=
OPENID_SESSION_SECRET=
OPENID_SCOPE="openid profile email"
OPENID_CALLBACK_URL=/oauth/openid/callback

OPENID_BUTTON_LABEL=
OPENID_IMAGE_URL=

#========================#
# Email Password Reset   #
#========================#

EMAIL_SERVICE=                  
EMAIL_HOST=                     
EMAIL_PORT=25                   
EMAIL_ENCRYPTION=               
EMAIL_ENCRYPTION_HOSTNAME=      
EMAIL_ALLOW_SELFSIGNED=         
EMAIL_USERNAME=                 
EMAIL_PASSWORD=                 
EMAIL_FROM_NAME=                
EMAIL_FROM=noreply@librechat.ai

#========================#
# Firebase CDN           #
#========================#

FIREBASE_API_KEY=
FIREBASE_AUTH_DOMAIN=
FIREBASE_PROJECT_ID=
FIREBASE_STORAGE_BUCKET=
FIREBASE_MESSAGING_SENDER_ID=
FIREBASE_APP_ID=

#===================================================#
#                        UI                         #
#===================================================#

APP_TITLE=LibreChat
# CUSTOM_FOOTER="My custom footer"
HELP_AND_FAQ_URL=https://librechat.ai

# SHOW_BIRTHDAY_ICON=true

#==================================================#
#                      Others                      #
#==================================================#
#   You should leave the following commented out   #

# NODE_ENV=

# REDIS_URI=
# USE_REDIS=

# E2E_USER_EMAIL=
# E2E_USER_PASSWORD=

```