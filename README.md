# Week14_Advanced_Web_Development_Maningo


## The Test Drive Activity

## Activity Information

| Item | Description |
|------|-------------|
| Activity Name | The Test Drive |
| Objective | Write a test that verifies the homepage returns HTTP 200 |
| Time Allotted | 15 minutes |
| Status | COMPLETED |

## Technologies Used

- PHP 8.2+
- CodeIgniter 4
- PHPUnit
- XAMPP
- Git & GitHub

## Project Structure

```
my-test-project/
├── app/
│   ├── Config/Routes.php
│   ├── Controllers/Home.php
│   └── Views/welcome_message.php
├── tests/
│   └── app/
│       └── Controllers/
│           └── HomeTest.php
├── public/
├── vendor/
└── writable/
```

## The Test Code

**File:** `tests/app/Controllers/HomeTest.php`

```php
<?php

namespace Tests\App\Controllers;

use CodeIgniter\Test\CIUnitTestCase;
use CodeIgniter\Test\FeatureTestTrait;

class HomeTest extends CIUnitTestCase
{
    use FeatureTestTrait;
    
    public function testHomePage()
    {
        $result = $this->get('/');
        $result->assertStatus(200);
    }
}
```

## How to Run the Test

```bash
# Go to project folder
cd C:\xampp\htdocs\my-test-project

# Run the test
vendor\bin\phpunit --filter HomeTest
```

## Expected Result

```
OK (1 test, 1 assertion)
```

## Step by Step Completion

| Step | Action | Status |
|------|--------|--------|
| 1 | Open HomeTest.php | DONE |
| 2 | Create testHomePage() method | DONE |
| 3 | Add assertion assertStatus(200) | DONE |
| 4 | Run vendor/bin/phpunit | DONE |

## How to Run the Website

```bash
php spark serve
```

Then open: `http://localhost:8080`

## Installation for Users

```bash
composer install
cp env .env
vendor/bin/phpunit --filter HomeTest
```

## GitHub Commands Used

```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/YOUR_USERNAME/my-test-project.git
git branch -M main
git push -u origin main
```

## .gitignore Contents

```
/vendor/
/writable/
.env
.vscode/
.DS_Store
Thumbs.db
*.log
```

## Test Result

| Test | Expected | Actual | Status |
|------|----------|--------|--------|
| Homepage HTTP Status | 200 | 200 | PASS |

## Completion Certificate

```
========================================
  THE TEST DRIVE ACTIVITY
  COMPLETED SUCCESSFULLY
  
  Test: HomeTest.php
  Method: testHomePage()
  Result: OK (1 test, 1 assertion)
========================================
```
