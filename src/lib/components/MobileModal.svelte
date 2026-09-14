<script lang="ts">
    import { IconX, IconCopy, IconClipboardCheck } from '@tabler/icons-svelte';
    import { Dialog, Portal, Toast, createToaster } from '@skeletonlabs/skeleton-svelte';
	const toaster = createToaster();

    const modalAnimation = 'transition transition-discrete opacity-0 translate-y-[100px] starting:data-[state=open]:opacity-0 starting:data-[state=open]:translate-y-[100px] data-[state=open]:opacity-100 data-[state=open]:translate-y-0';

    function copyLink() {
        navigator.clipboard.writeText('https://digitalbenin.org');
        toaster.info({
			description: 'Link copied in the clipboard!',
		})
  }
</script>

<Portal>
	<Dialog.Backdrop class="fixed inset-0 z-50 bg-surface-50-950/50" />
	<Dialog.Positioner class="fixed inset-0 z-50 flex justify-center items-center p-8">

		<Dialog.Content class="card bg-white w-full max-w-xl px-16 space-y-4 shadow-xl border-[1.5px] border-surface-200 {modalAnimation}">

			<header class="flex justify-between items-center py-16">
				<Dialog.Title class="font-semibold">Get Ọkpan for your computer</Dialog.Title>
				<Dialog.CloseTrigger class="btn-icon hover:preset-tonal">
					<IconX class="size-32" stroke="1.5" />
				</Dialog.CloseTrigger>
			</header>
				            
            <Dialog.Description>
                <p class="text-sm">
                    Open this website from your desktop device to start download it.
                </p>

                <p class="text-xs text-surface-500 pt-16">
                    Ọkpan is available for Windows and Mac computers.
                </p>
                
			</Dialog.Description>
				            
            <footer class="flex flex-col justify-end gap-8 py-12">
                <button type="button" class="btn bg-primary-600 text-white gap-8 py-12 px-24 w-full" onclick={copyLink}>
                    Copy link
                    <IconCopy class="size-20" stroke="1.5"/>
                </button>
			    <Dialog.CloseTrigger class="btn preset-outlined-surface-500 text-surface-500 py-12 px-24 w-full">Close</Dialog.CloseTrigger>
		    </footer>
                        
		</Dialog.Content>

	</Dialog.Positioner>
</Portal>


<Toast.Group {toaster}>
	{#snippet children(toast)}
		<Toast {toast} class='px-16 py-8'>
            <IconClipboardCheck class="size-24 text-primary-500" stroke="1.5" />
			<Toast.Message>
				<Toast.Description>{toast.description}</Toast.Description>
			</Toast.Message>
			<Toast.CloseTrigger />
		</Toast>
	{/snippet}
</Toast.Group>