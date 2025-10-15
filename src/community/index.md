---
layout: list.njk
title: "Community" 
permalink: /community/
---

{% set posts = collections.community %}

<p>If you'd like to submit anonymously, use the form below — submissions go to the admins for review.</p>

<form name="anon-sub" method="POST" data-netlify="true">
  <p><label>Title: <input type="text" name="title" required></label></p>
  <p><label>Due date: <input type="date" name="due_date" required></label></p>
  <p><label>Image URL: <input type="url" name="image"></label></p>
  <p><label>Message: <textarea name="message" required></textarea></label></p>
  <p><button type="submit">Submit for review</button></p>
</form>

