<script lang="ts">
	import { ToggleGroup } from "$lib";
	import { TextB, TextItalic, TextStrikethrough } from "$icons/index.js";

	let value: string[] | undefined = ["bold"];
</script>

<ToggleGroup.Root
	bind:value
	type="multiple"
	class="flex h-input items-center gap-x-0.5 rounded-card-sm border border-border bg-background px-[5px] py-1 shadow-mini"
>
	<ToggleGroup.Item
		aria-label="toggle bold"
		value="bold"
		class="inline-flex size-10 items-center justify-center rounded-9px bg-background transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=off]:text-foreground-alt data-[state=on]:text-foreground active:data-[state=on]:bg-dark-10"
	>
		<TextB class="size-6" />
	</ToggleGroup.Item>
	<ToggleGroup.Item
		aria-label="toggle italic"
		value="italic"
		class="inline-flex size-10 items-center justify-center rounded-9px bg-background transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=off]:text-foreground-alt data-[state=on]:text-foreground active:data-[state=on]:bg-dark-10"
	>
		<TextItalic class="size-6" />
	</ToggleGroup.Item>
	<ToggleGroup.Item
		aria-label="toggle strikethrough"
		value="strikethrough"
		class="inline-flex size-10 items-center justify-center rounded-9px bg-background transition-all hover:bg-muted active:scale-98 active:bg-dark-10 data-[state=on]:bg-muted data-[state=off]:text-foreground-alt data-[state=on]:text-foreground active:data-[state=on]:bg-dark-10"
	>
		<TextStrikethrough class="size-6" />
	</ToggleGroup.Item>
</ToggleGroup.Root>
