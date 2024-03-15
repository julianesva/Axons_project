```mermaid
classDiagram
    User "1" <|--  "*" Video : uploads
    Video "1" -- "1" Feedback : has

    class User {
        -UserID: String
        -User_name: String
        -Email: String
        -Password: String
        +UploadVideo()
        +ViewFeedback()
        +get_user_ID()
        +get_user_name()
        +get_user_email()
        +set_user_ID()
        +set_user_name()
        +set_user_email()
        +set_user_password()
    }
    class Video {
        -VideoID: String
        -Video_url: String
        -video_date: String
        -video_description: String
        +get_video_ID()
        +get_url()
        +get_date()
        +get_decription()
        +set_video_ID()
        +set_url()
        +set_date()
        +set_decription()
        +AddFeedback()

    }
    class Feedback {
        +FeedbackID
        +VideoID
        +get_fedback_ID()
        +get_video_ID()
        +set_fedback_ID()
        +set_video_ID()
    }
