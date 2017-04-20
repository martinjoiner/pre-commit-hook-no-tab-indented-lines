# Pre-commit hook for teams working on a mix of Windows and Mac machines

A pre-commit hook that does not pass tab-indented code or code indented with an uneven number of spaces. 

Avoiding tab-indentation is the best way to ensure code looks the same on all code editors/viewers including Mac, Windows, Vim and the GitHub website. 

## Exceptions

Exceptions are made for lines indented with an odd number of spaces where the first non-space character is an asterisk. This is so as to pass a standard multiline DocComment like this...

```php
/**
 * This function is great
 *
 * @param {string} $myString
 */
function printMock( $myString ){
	print $myString;
}
```

## How to use

Simply copy the file called __pre-commit__ into your repository's githooks folder (usually `.git/hooks/`) and it will be invoked on every commit. 

To learn more about githooks visit https://git-scm.com/docs/githooks 
