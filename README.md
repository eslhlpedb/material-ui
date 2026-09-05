# Accessibility

Material UI components are designed with accessibility in mind, adhering to WAI-ARIA standards.

## Key Considerations

### Screen Readers

Ensure that interactive elements without visible text labels (such as `IconButton` or standalone icons) include an explicit `aria-label` or `aria-labelledby` prop so screen readers can announce their purpose.

```jsx
// Good
<IconButton aria-label="delete">
  <DeleteIcon />
</IconButton>

// Good (using aria-labelledby)
<Typography id="trash-label" hidden>Move item to trash</Typography>
<IconButton aria-labelledby="trash-label">
  <DeleteIcon />
</IconButton>
```

### Color Contrast

Make sure the contrast ratio between text and background meets WCAG 2.1 AA standards (minimum 4.5:1 for normal text and 3:1 for large text).

### Focus Management

All interactive elements are focusable via keyboard navigation by default. Use `autoFocus` sparingly to prevent unexpected context switches for screen reader users.