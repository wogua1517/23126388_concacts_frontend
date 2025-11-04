# Frontend Code Style Guide (WeChat Mini Program)

## Source of Standards

This code style guide is based on the following widely adopted official and community standards:
- [Official WeChat Mini Program Coding Guidelines](https://developers.weixin.qq.com/miniprogram/dev/framework/)
- [Google JavaScript Style Guide](https://google.github.io/styleguide/jsguide.html)
- [Airbnb JavaScript Style Guide (ES6+)](https://github.com/airbnb/javascript)

All frontend code (`.js`, `.wxml`, `.wxss`) must comply with this guide.

---

## 1. JavaScript (Page Logic)

### Naming Conventions
- Use **camelCase** for variables and function names  
  `saveContact`, `onNameInput`  
- Use **UPPER_SNAKE_CASE** for constants  
  `const MAX_AVATAR_SIZE = 1024 * 1024;`

### Indentation & Formatting
- Use **2 spaces** for indentation (no tabs)
- Limit lines to **100 characters**
- Include trailing commas in multi-line objects/arrays

### Functions & Methods
- Page methods must be defined inside `Page({})`
- Prefer `async/await` over nested callbacks for asynchronous operations
- Event handlers should start with `on` or `handle` (e.g., `onPhoneInput`, `handleDelete`)

### Comments
- Add JSDoc-style comments above complex logic blocks:
  ```js
  /**
   * Uploads a temporary avatar to cloud storage and returns the file ID.
   * @returns {Promise<string|null>}
   */
  uploadAvatar() { ... }
