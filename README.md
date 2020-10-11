# survey-page

<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta name="Survey Page" content="FreeCodeCamp Survey Page Challenge">

    <style>

    @import url('https://fonts.googleapis.com/css?family=Poppins:200i,400&display=swap');

    :root {
      white: #f3f3f3;
      darkblue: rgb(27, 27, 50);
      darkblue-alpha: rgba(27, 27, 50, 0.8);
      green: #37af65;
    }

    *,
    *::before,
    *::after {
      box-sizing: border-box;
    }

    body {
      font-family: sans-serif;
      font-size: 1rem;
      font-weight: 400;
      line-height: 1.4;
      color: white;
      margin: 0;
    }


    #title {
      font-family: sans-serif;
      text-align: center;
      font-weight: 600;
      line-height: 1.2;
    }

    .header {
      padding: 0 0.625rem;
      margin-bottom: 1.875rem;
    }

    #description {
      text-align: center;
      font-size: 1.125rem;
    }

    .description {
      font-style: italic;
      font-weight: 200;
      text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.4);
    }

    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      height: 100%;
      width: 100%;
      z-index: -1;
      background: darkblue;
      background-image: linear-gradient(
          115deg,
          rgba(58, 58, 158, 0.8),
          rgba(136, 136, 206, 0.7)
        ),
        url(https://cdn.freecodecamp.org/testable-projects-fcc/images/survey-form-background.jpeg);
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center;
    }

    h1,
    p {
      margin-top: 10;
      margin-bottom: 0.5rem;
    }

    label {
      display: flex;
      align-items: center;
      font-size: 1.125rem;
      margin-bottom: 0.5rem;
      margin-top: 0.3rem;
    }

    form {
          background-color: darkblue;
          padding: 15px;
          margin: 10rem;
          border-radius: 5px;  
    }

    input,
    button,
    select,
    textarea {
      margin: 0;
      font-family: inherit;
      font-size: inherit;
      line-height: inherit;
    }

    p2 {
      display: flex;
      align-items: center;
      font-size: 1.125rem;
      margin-bottom: 0.5rem;
      margin-top: 0.3rem;
    }

    button {
      border: none;
    }

    .input-checkbox {
      display: inline-block;
      margin-right: 0.625rem;
      min-height: 1.25rem;
      min-width: 1.25rem;
    }

    .input-textarea {
      min-height: 120px;
      width: 100%;
      padding: 0.625rem;
      resize: vertical;
    }

    .submit-button {
      display: block;
      width: 100%;
      padding: 0.75rem;
      background: green;
      color: inherit;
      border-radius: 2px;
      cursor: pointer;
    }

    </style>

  </head>

<body>
  <main>
    <header class="header">
    <h1 id="title">FreeCodeCamp Survey Form</h1>
    <p class="description" id="description">Thankyou for helping us to improve the platform.</p>
    </header>

    <section>
    <form id="survey-form">
      <label id="name-label" for="name">Name</label>
      <input type="text" name="name" id="name" class="form-control" placeholder="Enter your name" required>

      <label id="email-label" for="email">Email</label>
      <input type="email" name="email" id="email" class="form-control" placeholder="Enter your email" required>

      <label id="number-label" for="number">Number</label>
      <input type="number" name="number" id="number" class="form-control" min="0" max="1000000000000000000" placeholder="Enter your number">
      <hr>

        <p2>Which option best describes your job title?</p2>
      <select id="dropdown" name="role" class="form-control">
        <option disabled selected value>Please select your current role</option>
        <option value="business">Business</option>
        <option value="marketing">Marketing</option>
        <option value="design">Design</option>
        <option value="other">Other</option>
      </select>
      <hr>

        <p2>Would you recommend FreeCodeCamp to a friend?</p2>
        <label>
          <input name="user-recommend" value="yes" type="radio" class="input-radio" checked>Yes</input>
        </label>

        <label>
          <input name="user-recommend" value="no" type="radio" class="input-radio">No</input>
        </label>
        <hr>

    <p2>Please check which program you use:</p2>

      <label for="github">
        <input id="github" value="github" type="checkbox" name="use" class="input-checkbox">GitHub</label>

      <label for="terminal">
        <input id="terminal" value="terminal" type="checkbox" name="use" class="input-checkbox">Terminal</label>

      <label for="repl-it">
        <input id="repl-it" value="repl-it" type="checkbox" name="use" class="input-checkbox">Repl.it</label>

    <label for="medium">
        <input id="medium" value="medium" type="checkbox" name="use" class="input-checkbox">Medium</label>

        <label for="other">
        <input id="other" value="other" type="checkbox" name="use" class="input-checkbox">Other</label>
        <hr>

    <p2>Do you have any additional comments?</p2>
    <textarea id="comments" name="comment" class="input-textarea" placeholder="Enter your comment here..."></textarea>


    <button type="submit" id="submit" class="submit-button">Submit</button>
      </form>
  </section>


  </main>
</body>

</html>
