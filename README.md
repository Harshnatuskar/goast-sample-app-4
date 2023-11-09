# Getting Started with Goast

A nextjs replicate app to test goastai's crash bot that can be used to demonstrate goast's ability to fix crashes.

## How to use this repository

1) Fork this repository if you haven't already. Generate an api key over replicate and save it in a .env.local file.
2) Go to https://app.goast.ai and click the button to add a repository. Make sure to install the goast Github App in the organization where this repository exists (Probably just on your user).
3) Copy this trace to put into goast (Or you can click the `Use sample stack trace` button in goast)
```
Here is the trace:
  ./src/app/page.js
   ReactServerComponentsError:
   You're importing a component that needs useState. It only works in a Client Component but none of      its parents are marked with "use client", so they're Server Components by default 
 1 │ // @react-env useClient
 2 │ import { useState } from "react";
   ·          ────────
 3 │ import Head from "next/head"; // @react-env useClient
 4 │ import Image from "next/image"; // @react-env useClient
 5 │ import styles from "../styles/Home.module.css";
```
4) Click `Generate Fix`

## About the stack trace

Goast can fix any stacktrace if it has access to the corresponding code. This means it can fix frontend or backend errors.

This example is a useState error in a nextjs component.

## Run this sample

If you want to see the crash in action, you can run this sample yourself by installing the dependencies with `npm install` and then running `npm run start`. 
 

