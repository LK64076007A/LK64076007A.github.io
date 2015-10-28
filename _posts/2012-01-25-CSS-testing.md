---
layout: post
date: 2012-01-25
title: Testing some CSS
tags: CSS
---

This is a <del>failed</del> <ins>semi-successful</ins> test of some CSS.

Warning. I have no formal training in CSS.

    // This raises the inserted text, rotates it slightly clockwise and moves it over the deleted text.
    ins {
        -webkit-transform: translate(-20px, -5px) rotate(15deg);
        display: inline-block;
        background: transparent;
        color: #0080C3;
        text-decoration: none;
    }

    // This creates the caret indicating the place to insert text.
    del:after {
        -webkit-transform: translate(0px, 1em) rotate(0deg);
        content:"^";
        display: inline-block;
        color: #0080C3;
    }

In my experience, there is no such thing as luck. You're all clear, kid. Let's blow this thing and go home! The Force is strong with this one. I have you now. All right. <del>Well, take care of yourself, Han.</del><ins>Error.</ins> I guess that's what you're best at, ain't it? I have traced the Rebel spies to her. Now she is my only link to finding their secret base.