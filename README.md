`ACCOUNT_NAME`, the `lower_bound` param of `getTableRows`, needs the variable for the account name of the logged in user.

```js
eos.getTableRows({
	json: true,
	code: "accountphoto",
	scope: "accountphoto",
	table: "photo",
	lower_bound: ACCOUNT_NAME
}).then((res) => {
	let photo = res.rows[0]
	// you can save and/or display the photo by reading "photo_hash"
});
```