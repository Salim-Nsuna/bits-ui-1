<script lang="ts">
	import { Separator, Toolbar } from "$lib";
	import {
		TextB,
		TextItalic,
		TextStrikethrough,
		TextAlignLeft,
		TextAlignCenter,
		TextAlignRight,
		Sparkle,
	} from "$icons/index.js";

	let text: string[] | undefined = ["bold"];
	let align: string | undefined;
</script>

<Toolbar.Root
	class="flex h-12 min-w-max items-center justify-center rounded-10px border border-border bg-background p-1 shadow-mini"
>
	<Toolbar.Group bind:value={text} type="multiple" class="flex items-center gap-x-0.5">
		<Toolbar.GroupItem
			aria-label="toggle bold"
			value="bold"
			class="inline-flex size-10 items-center justify-center rounded-9px bg-background text-foreground/60 transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=on]:text-foreground/80 active:data-[state=on]:bg-dark-10"
		>
			<TextB class="size-6" />
		</Toolbar.GroupItem>
		<Toolbar.GroupItem
			aria-label="toggle italic"
			value="italic"
			class="inline-flex size-10 items-center justify-center rounded-9px bg-background text-foreground/60 transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=on]:text-foreground/80 active:data-[state=on]:bg-dark-10"
		>
			<TextItalic class="size-6" />
		</Toolbar.GroupItem>
		<Toolbar.GroupItem
			aria-label="toggle strikethrough"
			value="strikethrough"
			class="inline-flex size-10 items-center justify-center rounded-9px bg-background text-foreground/60 transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=on]:text-foreground/80 active:data-[state=on]:bg-dark-10"
		>
			<TextStrikethrough class="size-6" />
		</Toolbar.GroupItem>
	</Toolbar.Group>

	<Separator.Root class="-my-1 mx-1 w-[1px] self-stretch bg-dark-10" />

	<Toolbar.Group bind:value={align} type="single" class="flex items-center gap-x-0.5">
		<Toolbar.GroupItem
			aria-label="align left"
			value="left"
			class="inline-flex size-10 items-center justify-center rounded-9px bg-background text-foreground/60 transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=on]:text-foreground/80 active:data-[state=on]:bg-dark-10"
		>
			<TextAlignLeft class="size-6" />
		</Toolbar.GroupItem>
		<Toolbar.GroupItem
			aria-label="align center"
			value="center"
			class="inline-flex size-10 items-center justify-center rounded-9px bg-background text-foreground/60 transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=on]:text-foreground/80 active:data-[state=on]:bg-dark-10"
		>
			<TextAlignCenter class="size-6" />
		</Toolbar.GroupItem>
		<Toolbar.GroupItem
			aria-label="align right"
			value="right"
			class="inline-flex size-10 items-center justify-center rounded-9px bg-background text-foreground/60 transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=on]:text-foreground/80 active:data-[state=on]:bg-dark-10"
		>
			<TextAlignRight class="size-6" />
		</Toolbar.GroupItem>
	</Toolbar.Group>

	<Separator.Root class="-my-1 mx-1 w-[1px] self-stretch bg-dark-10" />

	<div class="flex items-center">
		<Toolbar.Button
			class="inline-flex items-center justify-center rounded-9px px-3 py-2 text-sm  font-medium text-foreground/80 transition-all hover:bg-muted active:scale-98 active:bg-dark-10"
		>
			<Sparkle class="mr-2 size-6" />
			<span> Ask AI </span>
		</Toolbar.Button>
	</div>
</Toolbar.Root>
