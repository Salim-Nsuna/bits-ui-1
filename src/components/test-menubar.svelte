<script>
	import { Menubar } from "$lib";
	let bookmarks = false;
	let fullUrls = true;
	const profileRadioValue = "benoit";
</script>

<Menubar.Root>
	<Menubar.Menu>
		<Menubar.Trigger>File</Menubar.Trigger>
		<Menubar.Content>
			<Menubar.Item>New Tab</Menubar.Item>
			<Menubar.Item>New Window</Menubar.Item>
			<Menubar.Item>New Incognito Window</Menubar.Item>
			<Menubar.Separator />
			<Menubar.Sub>
				<Menubar.SubTrigger>Share</Menubar.SubTrigger>
				<Menubar.SubContent>
					<Menubar.Item>Email link</Menubar.Item>
					<Menubar.Item>Messages</Menubar.Item>
					<Menubar.Item>Notes</Menubar.Item>
				</Menubar.SubContent>
			</Menubar.Sub>
			<Menubar.Separator />
			<Menubar.Item>Print...</Menubar.Item>
		</Menubar.Content>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Trigger>Edit</Menubar.Trigger>
		<Menubar.Content>
			<Menubar.Item>Undo</Menubar.Item>
			<Menubar.Item>Redo</Menubar.Item>
			<Menubar.Separator />
			<Menubar.Sub>
				<Menubar.SubTrigger>Find</Menubar.SubTrigger>
				<Menubar.SubContent>
					<Menubar.Item>Search the web</Menubar.Item>
					<Menubar.Separator />
					<Menubar.Item>Find...</Menubar.Item>
					<Menubar.Item>Find Next</Menubar.Item>
					<Menubar.Item>Find Previous</Menubar.Item>
				</Menubar.SubContent>
			</Menubar.Sub>
			<Menubar.Separator />
			<Menubar.Item>Cut</Menubar.Item>
			<Menubar.Item>Copy</Menubar.Item>
			<Menubar.Item>Paste</Menubar.Item>
		</Menubar.Content>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Trigger>View</Menubar.Trigger>
		<Menubar.Content>
			<Menubar.CheckboxItem bind:checked={bookmarks}>Always Show Bookmarks Bar</Menubar.CheckboxItem
			>
			<Menubar.CheckboxItem bind:checked={fullUrls}>Always Show Full URLs</Menubar.CheckboxItem>
			<Menubar.Separator />
			<Menubar.Item>Reload</Menubar.Item>
			<Menubar.Item>Force Reload</Menubar.Item>
			<Menubar.Separator />
			<Menubar.Item>Toggle Fullscreen</Menubar.Item>
			<Menubar.Separator />
			<Menubar.Item>Hide Sidebar</Menubar.Item>
		</Menubar.Content>
	</Menubar.Menu>
	<Menubar.Menu>
		<Menubar.Trigger>Profiles</Menubar.Trigger>
		<Menubar.Content>
			<Menubar.RadioGroup value={profileRadioValue}>
				<Menubar.RadioItem value="andy">Andy</Menubar.RadioItem>
				<Menubar.RadioItem value="benoit">Benoit</Menubar.RadioItem>
				<Menubar.RadioItem value="Luis">Luis</Menubar.RadioItem>
			</Menubar.RadioGroup>
			<Menubar.Separator />
			<Menubar.Item>Edit...</Menubar.Item>
			<Menubar.Separator />
			<Menubar.Item>Add Profile...</Menubar.Item>
		</Menubar.Content>
	</Menubar.Menu>
</Menubar.Root>
