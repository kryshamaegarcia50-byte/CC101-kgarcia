# Multi-Tier Architecture

## What is a Two-Tier Architecture?

A Two-Tier Architecture is a system design that separates an application into two main parts: the Web/Application Tier and the Database Tier. Each tier has a specific responsibility and communicates with the other to provide the services needed by users.

## The Web/Application Tier

The Web/Application Tier handles user interactions and displays the application's user interface. It receives HTTP requests from users' browsers, processes application logic, and communicates with the database when information needs to be retrieved or saved.

## The Database Tier

The Database Tier stores and manages persistent data, such as user accounts, passwords in securely hashed form, and application records. It responds to database queries from the Web/Application Tier and helps ensure that information remains available even after the application restarts.

## Why Separate Them?

Separating the web server and database into two containers makes the application easier to manage, update, and troubleshoot. It also allows each service to use its own resources and security settings, reducing the risk of exposing the database directly to users. If one service needs to be restarted or scaled, it can often be managed independently of the other.
