erDiagram
    AUTHOR {
        int AuthorID PK
        string Name
        string URL
    }
    PUBLICATION {
        int PubID PK
        string Title
        string Type
    }
    BOOK {
        int BookID PK
        string Title
    }
    JOURNAL {
        int JournalID PK
        string Title
    }
    PROCEEDINGS {
        int ProceedingsID PK
        string Title
    }
    ARTICLE {
        int ArticleID PK
        string Title
    }

    AUTHOR ||--o{ PUBLICATION : "Writes"
    AUTHOR ||--o| JOURNAL : "ChiefEditor"
    AUTHOR ||--o| PROCEEDINGS : "ChiefEditor"
    BOOK ||--o{ ARTICLE : "Contains"
    JOURNAL ||--o{ ARTICLE : "Contains"
    PROCEEDINGS ||--o{ ARTICLE : "Contains"
