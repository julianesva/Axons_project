```mermaid
classDiagram
    User "1" <|--  "*" Video : uploads
    Video "1" <|-- "1" Feedback : has

    class User {
        -UserID: String
        -User_name: String
        -Email: String
        -Password: String
        +UploadVideo()
        +ViewFeed_His()
        +Authenticate_log()
        +Sign_up()
        +get_user_ID()
        +get_user_name()
        +get_email()
        +get_password()
        +set_user_ID()
        +set_user_name()
        +set_email()
        +set_password()
    }
    class Video {
        -VideoID: String
        -Video_url: String
        -video_date: String
        -videoai_resp: String
        +transcript_gen()
        +AddFeedback()
        +get_video_ID()
        +get_url()
        +get_date()
        +get_decription()
        +set_video_ID()
        +set_url()
        +set_date()
        +set_decription()
    }
    class Feedback {
        -FeedbackID: String
        -Feedback_result: String
        +get_fedback_ID()
        +set_fedback_ID()
    }
