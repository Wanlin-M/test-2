    <!DOCTYPE html>

<html lang="zh-TW">

<head>

  <meta charset="UTF-8">

  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>英語發音教學評分系統 (雲端連動版)</title>

  <style>

    *, *::before, *::after {

      box-sizing: border-box;

    }


    :root {

      --primary: #3498db;

      --success: #2ecc71;

      --warning: #f1c40f;

      --danger: #e74c3c;

      --purple: #8e44ad;

      --orange: #e67e22;

      --teal: #1abc9c;

      --dark: #1e293b;

      --light-bg: #f8fafc;

      --border: #cbd5e1;

    }


    body {

      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;

      background-color: #f0f4f8;

      color: var(--dark);

      margin: 0;

      padding: 30px 15px;

      display: flex;

      flex-direction: column;

      align-items: center;

    }


    .inapp-warning {

      display: none;

      background-color: #fff3cd;

      color: #856404;

      border: 1px solid #ffeeba;

      padding: 12px;

      border-radius: 8px;

      margin-bottom: 15px;

      width: 100%;

      max-width: 700px;

      font-size: 14px;

      line-height: 1.5;

      text-align: center;

    }


    .instructor-card {

      background: white;

      padding: 30px 25px;

      border-radius: 20px;

      box-shadow: 0 15px 35px rgba(0,0,0,0.08);

      width: 100%;

      max-width: 700px;

      position: relative;

    }


    .header-container {

      display: flex;

      justify-content: center;

      align-items: center;

      position: relative;

      margin-bottom: 20px;

    }


    h1 {

      text-align: center;

      color: var(--dark);

      font-size: 24px;

      margin: 0;

      font-weight: 700;

    }


    .btn-teacher-lock {

      position: absolute;

      right: 0;

      background: transparent;

      border: 1px solid #cbd5e1;

      color: #64748b;

      padding: 4px 10px;

      font-size: 12px;

      border-radius: 20px;

      cursor: pointer;

      transition: all 0.2s;

    }


    .btn-teacher-lock:hover {

      background: #f1f5f9;

      color: var(--dark);

    }


    .teacher-panel {

      display: none; 

      background: #eef6fb;

      border: 1px solid #bee3f8;

      border-radius: 12px;

      padding: 15px;

      margin-bottom: 20px;

      animation: fadeIn 0.3s ease-in-out;

    }


    .panel-title {

      font-size: 14px;

      font-weight: 700;

      color: var(--dark);

      margin-bottom: 10px;

      display: flex;

      align-items: center;

      gap: 5px;

    }


    .teacher-actions {

      display: flex;

      gap: 10px;

      flex-wrap: wrap;

      align-items: center;

    }


    .btn-file-label {

      background-color: var(--teal);

      color: white;

      padding: 8px 14px;

      border-radius: 6px;

      font-size: 13px;

      font-weight: 600;

      cursor: pointer;

      display: inline-block;

      transition: background 0.2s;

    }


    .btn-file-label:hover {

      background-color: #16a085;

    }


    .btn-random {

      background-color: var(--orange);

      color: white;

      padding: 8px 14px;

      border-radius: 6px;

      font-size: 13px;

      font-weight: 600;

      border: none;

      cursor: pointer;

      transition: background 0.2s;

    }


    .btn-random:hover {

      background-color: #d35400;

    }


    .bank-status {

      font-size: 12px;

      color: #64748b;

      margin-top: 8px;

    }


    .student-info-form {

      display: grid;

      grid-template-columns: repeat(3, minmax(0, 1fr));

      gap: 10px;

      background: var(--light-bg);

      padding: 15px;

      border-radius: 12px;

      border: 1px solid var(--border);

      margin-bottom: 20px;

      width: 100%;

    }


    .form-group {

      display: flex;

      flex-direction: column;

      text-align: left;

      width: 100%;

    }


    .form-group label {

      font-size: 13px;

      font-weight: 600;

      margin-bottom: 4px;

      color: var(--dark);

      white-space: nowrap;

    }


    .form-group label::after {

      content: " *";

      color: var(--danger);

    }


    .form-group input {

      width: 100%;

      padding: 8px 12px;

      font-size: 14px;

      border: 1px solid var(--border);

      border-radius: 6px;

      outline: none;

    }


    .form-group input:focus {

      border-color: var(--primary);
