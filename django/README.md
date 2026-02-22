# Django Backend - Surveillance System

This is the Django REST API backend for the surveillance system, implementing person re-identification using YOLOv8 and deep learning models.

## Features

- RESTful API for user management, camera control, and re-identification
- Person re-identification using YOLOv8 object detection and deep learning
- Real-time video processing with Deep SORT tracking
- SQLite database for data storage
- CORS enabled for frontend communication
- Email notifications

## Prerequisites

- Python 3.8 or higher
- pip (Python package manager)

## Installation

1. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   venv\Scripts\activate  # On Windows
   # source venv/bin/activate  # On macOS/Linux
   ```

2. Navigate to the django directory:
   ```bash
   cd django/surveillance_system
   ```

3. Install dependencies:
   ```bash
   pip install django channels opencv-python torch torchvision torchaudio scipy ultralytics deep-sort-realtime torchreid gdown django-cors-headers tensorboard
   ```

   Or create a requirements.txt file with the above packages and run:
   ```bash
   pip install -r requirements.txt
   ```

4. Apply database migrations:
   ```bash
   python manage.py migrate
   ```

5. (Optional) Create a superuser for admin access:
   ```bash
   python manage.py createsuperuser
   ```

## Configuration

- Update `settings.py` for production:
  - Set `DEBUG = False`
  - Configure `ALLOWED_HOSTS`
  - Set secure `SECRET_KEY`
  - Configure email settings for notifications

## Usage

1. Start the Django development server:
   ```bash
   python manage.py runserver
   ```

   The API will be available at `http://127.0.0.1:8000/`

2. API Endpoints:
   - `/api/auth/` - Authentication (login, register, logout)
   - `/api/users/` - User management
   - `/api/cameras/` - Camera management
   - `/api/reid/` - Person re-identification operations

## Project Structure

- `core/models.py` - Database models (User, Camera, ReIDLog, etc.)
- `core/views/` - API view handlers
- `core/utils/reid_processor.py` - Re-identification processing logic
- `input_videos/` - Directory for input video files
- `output_videos/` - Directory for processed output videos

## Dependencies

- Django 5.1+
- OpenCV for computer vision
- PyTorch for deep learning
- Ultralytics YOLOv8 for object detection
- Deep SORT for object tracking
- TorchReID for person re-identification

## API Documentation

The API uses Django REST framework. Authentication is handled via token-based auth.

## Troubleshooting

- Ensure all Python packages are installed correctly
- Check that the YOLOv8 model file (`yolov8n.pt`) is present
- Verify database migrations are applied
- For video processing, ensure input videos are in supported formats (MP4, AVI)