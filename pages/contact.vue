<template>
  <div class="contact">
    <h1>Contact</h1>

    <p>LinkedIn: <a href="https://www.linkedin.com/in/joshua-m-b-a-b8a8b8a9/">Joshua M. B. A.</a></p>
    <p>Phone: (816) 532-9076</p>
    <p>Email: silver@gmail.com</p>

    <h2>Send me an email:</h2>
    <form>
      <div class="form-group">
        <label for="name">Name</label>
        <input type="text" class="form-control" id="name" placeholder="Enter name">
      </div>
      <div class="form-group">
        <label for="email">Email address</label>
        <input type="email" class="form-control" id="email" placeholder="Enter email">
      </div>
      <div class="form-group">
        <label for="message">Message</label>
        <textarea class="form-control" id="message" rows="3"></textarea>
      </div>
      <button type="submit" class="btn btn-primary">Submit</button>
    </form>
  </div>
</template>
