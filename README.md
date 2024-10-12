


```
python main.py -i <image_url> -db <database_path>
```

# tests


```
pytest tests/
```

Or run specific test files with:

```
pytest tests/test_db_manager.py
```

These tests cover the basic functionality of each module in our project. We use pytest fixtures for setup, mocking for external dependencies, and various assertions to check the expected behavior of our functions.

Some notes on the tests:
We use in-memory SQLite database for testing the DBManager to avoid affecting any real database.
External API calls (like in VLM and OCRExtractor) are mocked to avoid making real network requests during testing.
Image processing in TextDetector and FeatureExtractor is also mocked, as we don't want to depend on real images for our tests.
We test both normal scenarios and some edge cases (like invalid inputs) where applicable.
