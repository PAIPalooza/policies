### SnapSight Product Requirements Document (PRD)

#### Project Code Name: SnapSight

### Overview

Navigating the intricate realm of digital engagement requires robust tools. SnapSight, our platform tailored for both influencers and marketers, is built on a state-of-the-art tech stack that prioritizes performance and scalability. At its core, the platform boasts advanced analytics capabilities, enabling users to dissect audience behaviors and preferences. Features such as real-time audience insights, A/B testing modules, and predictive engagement analytics stand out, ensuring content strategies are both relevant and impactful. 

For those keen on the tech specifics, we've integrated Python-based machine learning algorithms, a React frontend for responsiveness, and a Node.js backend for optimal performance. Whether you're an influencer aiming to amplify your reach or a marketer refining campaigns, SnapSight's blend of features and cutting-edge technology ensures you're always a step ahead in the digital game.

### User Stories

**1. User Authentication:**
- As a user, I want to sign up using my email so that I can access the platform.
- As a user, I want to log in to the platform to access my data and insights.

**2. Audience Analyzer:**
- As a marketer, I want to input my targeting specifications so that I can get detailed insights about my audience.
- As a marketer, I want to see a visual representation of my audience data so that I can understand it better.

**3. Audience Size Estimator:**
- As a marketer, I want to input my targeting spec or ad squad to estimate the size of my audience.
- As a marketer, I want to see the estimated range of my audience size so that I can plan my campaigns accordingly.

**4. Interactive Dashboard:**
- As a user, I want to see dynamic charts and graphs of my audience data so that I can analyze it effectively.
- As a user, I want to filter and refine the data on my dashboard to focus on specific data points.

**5. Campaign Optimizer:**
- As a marketer, I want the platform to analyze my provided targeting specs and suggest optimizations.
- As a marketer, I want to see recommendations on how to improve my campaign targeting for better results.

**6. Historical Trends:**
- As a user, I want to see how my audience data has changed over time to identify trends.
- As a user, I want to select specific date ranges to focus on certain periods.

### Data Model

**1. Users**
- `userID`: Unique identifier for the user (String)
- `email`: User's email address (String)
- `displayName`: User's display name (String)
- `createdAt`: Timestamp of account creation (Timestamp)
- `lastLogin`: Timestamp of the last login (Timestamp)

**2. Audience Data**
- `audienceID`: Unique identifier for the audience data (String)
- `userID`: Reference to the user who fetched this data (String)
- `baseSpec`: The base targeting specifications (String)
- `targetingSpec`: The targeting specifications (String)
- `insights`: 
  - `target_audience`:
    - `audience_size_minimum`: Minimum audience size (Number)
    - `audience_size_maximum`: Maximum audience size (Number)
  - `reference_audience`:
    - `audience_size_minimum`: Minimum size of the reference audience (Number)
    - `audience_size_maximum`: Maximum size of the reference audience (Number)
  - `categories`:
    - `demographics`:
      - `distribution`:
        - `age_groups`:
          - `id`: Identifier for the age group (String)
          - `name`: Name of the age group (String)
          - `target_audience_percent`: Percent of target audience in this age group (Number)
          - `reference_audience_percent`: Percent of reference audience in this age group (Number)
          - `target_index_to_reference`: Index comparing target to reference audience (Number)
          - `metadata`: Additional metadata if any (Object)
        - `gender`:
          - `id`: Identifier for the gender (String)
          - `name`: Name of the gender (String)
          - `target_audience_percent`: Percent of target audience of this gender (Number)
          - `reference_audience_percent`: Percent of reference audience of this gender (Number)
          - `target_index_to_reference`: Index comparing target to reference audience (Number)
          - `metadata`: Additional metadata if any (Object)
        - `languages`:
          - `id`: Identifier for the language (String)
          - `name`: Name of the language (String)
          - `target_audience_percent`: Percent of target audience speaking this language (Number)
          - `reference_audience_percent`: Percent of reference audience speaking this language (Number)
          - `target_index_to_reference`: Index comparing target to reference audience (Number)
          - `metadata`: Additional metadata if any (Object)
        - `advanced_demographics`:
          - `id`: Identifier for the advanced demographic (String)
          - `name`: Name of the advanced demographic category (String)
          - `target_audience_percent`: Percent of target audience in this demographic category (Number)
          - `reference_audience_percent`: Percent of reference audience in this demographic category (Number)
          - `target_index_to_reference`: Index comparing target to reference audience (Number)
          - `metadata`: Additional metadata if any (Object)
  - `createdAt`: Timestamp of when the data was fetched (Timestamp)

**3. Campaigns**
- `campaignID`: Unique identifier for the campaign (String)
- `userID`: Reference to the user who created the campaign (String)
- `name`: Name of the campaign (String)
- `targeting`: Targeting specifications for the campaign (String)
- `status`: Status of the campaign (e.g., active, paused, etc.) (String)
- `createdAt`: Timestamp of campaign creation (Timestamp)

---
### Product Requirements Document (PRD) for BookMarkShare

#### 1. **Project Overview**
BookMarkShare is a modern social bookmarking application inspired by Del.icio.us. It allows users to save, manage, and share bookmarks, as well as engage with the community through tags, comments, likes, and notifications. The project will be developed using the MERN (MongoDB, Express, React, Node.js) stack with a Test-Driven Development (TDD) approach.

#### 2. **Goals and Objectives**
- **Goal**: To create a user-friendly platform for bookmarking, organizing, and sharing web content.
- **Objectives**:
  - Implement secure user registration and authentication.
  - Allow users to create, edit, delete, and organize bookmarks.
  - Enable tagging, liking, and commenting on bookmarks.
  - Provide a notification system for user interactions.
  - Develop a Chrome extension for quick bookmarking.

#### 3. **Features and Functionalities**

##### 3.1 User Management
- **User Registration**: Allow new users to create accounts with a username, email, and password.
- **User Login**: Authenticate users with their email and password.
- **Profile Management**: Enable users to update their profile information and settings.
- **Authentication**: Secure user authentication with JWT.

##### 3.2 Bookmark Management
- **Create Bookmark**: Users can save new bookmarks with title, URL, description, and tags.
- **Edit Bookmark**: Users can update the details of existing bookmarks.
- **Delete Bookmark**: Users can remove bookmarks from their collection.
- **View Bookmarks**: Users can view their bookmarks in an organized manner.

##### 3.3 Tag Management
- **Create Tag**: Users can create tags to categorize bookmarks.
- **Edit Tag**: Users can update the name of existing tags.
- **Delete Tag**: Users can remove tags.
- **View Tags**: Users can view all tags they have created.

##### 3.4 Social Features
- **Like Bookmarks**: Users can like bookmarks.
- **Comment on Bookmarks**: Users can add comments to bookmarks.
- **View Likes and Comments**: Users can view likes and comments on their bookmarks.

##### 3.5 Notification System
- **Notifications**: Users receive notifications for likes, comments, and follows.

##### 3.6 Chrome Extension
- **Quick Bookmarking**: Users can quickly save bookmarks from their browser.
- **Manage Bookmarks**: Users can view and manage their bookmarks directly from the extension.

#### 4. **Technology Stack**
- **Backend**: Node.js, Express, MongoDB
- **Frontend**: React
- **Testing**: Jest, Supertest
- **Chrome Extension**: JavaScript, HTML, CSS

#### 5. **Development Approach**
- **Methodology**: Agile with Test-Driven Development (TDD)
- **Sprints**: 
  - Sprint 1: Backend API
  - Sprint 2: Frontend
  - Sprint 3: Chrome Plugin

### Data Model

#### User
```json
{
  "User": {
    "username": "string",
    "email": "string",
    "password_hash": "string",
    "bio": "string",
    "profile_image_url": "string",
    "followers_count": "number",
    "following_count": "number",
    "is_active": "boolean",
    "last_login": "date",
    "settings": "object",
    "createdAt": "date",
    "updatedAt": "date"
  }
}
```

#### Bookmark
```json
{
  "Bookmark": {
    "title": "string",
    "url": "string",
    "description": "string",
    "tags": ["string"],
    "user_id": "ObjectId",
    "likes_count": "number",
    "comments_count": "number",
    "is_public": "boolean",
    "createdAt": "date",
    "updatedAt": "date"
  }
}
```

#### Tag
```json
{
  "Tag": {
    "name": "string",
    "user_id": "ObjectId",
    "createdAt": "date",
    "updatedAt": "date"
  }
}
```

#### Like
```json
{
  "Like": {
    "user_id": "ObjectId",
    "bookmark_id": "ObjectId",
    "createdAt": "date"
  }
}
```

#### Comment
```json
{
  "Comment": {
    "user_id": "ObjectId",
    "bookmark_id": "ObjectId",
    "content": "string",
    "createdAt": "date",
    "updatedAt": "date"
  }
}
```

#### Notification
```json
{
  "Notification": {
    "user_id": "ObjectId",
    "type": "string",
    "data": "object",
    "read": "boolean",
    "createdAt": "date",
    "updatedAt": "date"
  }
}
```

