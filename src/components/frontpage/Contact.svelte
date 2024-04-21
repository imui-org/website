<div class="text-center rounded-lg bg-white p-8 shadow-lg lg:p-12">
	<form action="#" class="space-y-4">
		<div>
			<label class="sr-only" for="name">Name</label>
			<input
				class="w-full rounded-lg p-3 text-sm ring-1 ring-gray-400"
				placeholder="Name"
				type="text"
				id="name"
			/>
		</div>
		<div>
			<div>
				<label class="sr-only" for="email">Email</label>
				<input
					class="w-full rounded-lg p-3 text-sm ring-1 ring-gray-400"
					placeholder="Email Adresse"
					type="email"
					id="email"
				/>
			</div>
		</div>
		<div>
			<label class="sr-only" for="message">Nachricht</label>
			<textarea
				class="w-full rounded-lg p-3 text-sm ring-1 ring-gray-400"
				placeholder="Nachricht"
				rows="8"
				id="message"
			></textarea>
		</div>
		<div>
			<label for="Option1" class="flex cursor-pointer items-start gap-4">
				<div class="flex items-center">
					&#8203;
					<input type="checkbox" class="size-4 rounded border-gray-400" id="Option1" />
				</div>
				<div>
					<p class="text-gray-900">
						Ich habe die Datenschutzerklärung gelesen und zur Kenntnis genommen.
					</p>
				</div>
			</label>
		</div>
		<div class="mt-4">
			<button
				type="submit"
				class="inline-block w-full rounded-lg bg-teal-400 px-5 py-3 font-medium text-white sm:w-auto"
			>
				Senden
			</button>
		</div>
	</form>
</div>
