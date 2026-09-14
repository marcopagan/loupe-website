<script lang="ts">
    import { IconX, IconDownload, IconBrandWindows, IconBrandApple, IconInfoCircle } from '@tabler/icons-svelte';
    import { Dialog, Portal } from '@skeletonlabs/skeleton-svelte';

    const modalAnimation = 'transition transition-discrete opacity-0 translate-y-[100px] starting:data-[state=open]:opacity-0 starting:data-[state=open]:translate-y-[100px] data-[state=open]:opacity-100 data-[state=open]:translate-y-0';
    let selectedOption = $state(0);

    const options = ['None selected', 'Windows selected!', 'MacOS Silicon selected!', 'MacOS x86 selected!'];
</script>

<Portal>
	<Dialog.Backdrop class="fixed inset-0 z-50 bg-surface-50-950/50" />
	<Dialog.Positioner class="fixed inset-0 z-50 flex justify-center items-center p-4">

		<Dialog.Content class="card bg-white w-full max-w-xl px-24 py-8 space-y-4 shadow-xl border-[1.5px] border-surface-200 {modalAnimation}">

			<header class="flex justify-between items-center py-24">
				<Dialog.Title class="text-xl font-semibold">Get Ọkpan for your platform</Dialog.Title>
				<Dialog.CloseTrigger class="btn-icon hover:preset-tonal">
					<IconX class="size-32" stroke="1.5" />
				</Dialog.CloseTrigger>
			</header>
				            
            <Dialog.Description>
				<form class="space-y-2 flex flex-col gap-16">
	                        
                    <label class="flex items-center space-x-2 p-16 rounded-xl border-[1.5px] border-surface-100 gap-24 download-radio-item cursor-pointer">
		                <input class="radio size-32" type="radio" checked name="radio-direct" value="1" style="display: none;" bind:group={selectedOption}/>
                        <div class="p-12 rounded-xl bg-blue-800">
                            <IconBrandWindows class="size-32 text-white" stroke="1.5" />
                        </div>
		                <p class="font-semibold">Windows</p>
	                </label>

                    <label class="flex items-center space-x-2 p-16 rounded-xl border-[1.5px] border-surface-100 gap-24 download-radio-item cursor-pointer">
		                <input class="radio size-32" type="radio" name="radio-direct" value="2" style="display: none;" bind:group={selectedOption}/>
                        <div class="p-12 rounded-xl bg-surface-500">
                            <IconBrandApple class="size-32 text-white" stroke="1.5" />
                        </div>
                        <div>
		                    <p><span class="font-semibold">MacOS Silicon</span> (M Series)</p>
                            <p class="text-sm text-surface-500 pt-4">Devices released after 2020-2021</p>
                        </div>
	                </label>

                    <label class="flex items-center space-x-2 p-16 rounded-xl border-[1.5px] border-surface-100 gap-24 download-radio-item cursor-pointer">
		                <input class="radio size-32" type="radio" name="radio-direct" value="3" style="display: none;" bind:group={selectedOption}/>
                        <div class="p-12 rounded-xl bg-surface-500">
                            <IconBrandApple class="size-32 text-white" stroke="1.5" />
                        </div>
                        <div>
		                    <p><span class="font-semibold">MacOS x86</span> (Intel)</p>
                            <p class="text-sm text-surface-500 pt-4">Devices released before 2020</p>
                        </div>
	                </label>
                </form>

                <div class="flex gap-4 py-24 px-12">
                    <IconInfoCircle class="size-14 text-surface-500 h-20" stroke="1.5" />
                    <p class="text-sm text-surface-500">You are not sure about which Mac do you have? <a class="underline" href="https://support.apple.com/en-us/116943" title="Apple Support" target="_blank" rel="noopener">See here</a></p>
                </div>
                
			</Dialog.Description>
				            
            <footer class="flex justify-end gap-8 py-12">
			    <Dialog.CloseTrigger class="btn lg:btn-lg preset-outlined-surface-500 text-surface-500 py-16 px-24">Close</Dialog.CloseTrigger>
			    <button type="button" class="btn lg:btn-lg bg-primary-600 text-white gap-8 py-16 px-24" disabled={selectedOption !== 0 ? false : true} onclick={() => alert(options[selectedOption])}>
                    Download
                    <IconDownload class="size-18" stroke="1.5"/>
                </button>
		    </footer>
                        
		</Dialog.Content>

	</Dialog.Positioner>
</Portal>